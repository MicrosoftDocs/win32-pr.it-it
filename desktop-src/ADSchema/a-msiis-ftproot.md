---
title: MS-IIS-FTP-root (attributo)
description: Questo attributo determina la condivisione file server. Viene usato in combinazione con MS-IIS-FTP-dir per determinare la home directory dell'utente FTP.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-IIS-FTP-root
- msIIS-schema AD attributo FTPRoot
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480329"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="e7cd5-106">MS-IIS-FTP-root (attributo)</span><span class="sxs-lookup"><span data-stu-id="e7cd5-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="e7cd5-107">Questo attributo determina la condivisione file server.</span><span class="sxs-lookup"><span data-stu-id="e7cd5-107">This attribute determines the file server share.</span></span> <span data-ttu-id="e7cd5-108">Viene usato in combinazione con MS-IIS-FTP-dir per determinare la home directory dell'utente FTP.</span><span class="sxs-lookup"><span data-stu-id="e7cd5-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="e7cd5-109">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-109">Entry</span></span> | <span data-ttu-id="e7cd5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cd5-111">CN</span><span class="sxs-lookup"><span data-stu-id="e7cd5-111">CN</span></span>                | <span data-ttu-id="e7cd5-112">MS-IIS-FTP-radice</span><span class="sxs-lookup"><span data-stu-id="e7cd5-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="e7cd5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e7cd5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e7cd5-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="e7cd5-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="e7cd5-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e7cd5-115">Size</span></span>              | <span data-ttu-id="e7cd5-116">30-50 caratteri (15-25 caratteri Unicode per ogni proprietà)</span><span class="sxs-lookup"><span data-stu-id="e7cd5-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="e7cd5-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-117">Update Privilege</span></span>  | <span data-ttu-id="e7cd5-118">Amministratore di dominio & sistema locale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="e7cd5-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-119">Update Frequency</span></span>  | <span data-ttu-id="e7cd5-120">Questa proprietà viene impostata quando l'amministratore crea il sito Web e imposta l'isolamento FTP.</span><span class="sxs-lookup"><span data-stu-id="e7cd5-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="e7cd5-121">In questo modo si modifica raramente.</span><span class="sxs-lookup"><span data-stu-id="e7cd5-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="e7cd5-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-122">Attribute-Id</span></span>      | <span data-ttu-id="e7cd5-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="e7cd5-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="e7cd5-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e7cd5-124">System-Id-Guid</span></span>    | <span data-ttu-id="e7cd5-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="e7cd5-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="e7cd5-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7cd5-126">Syntax</span></span>            | [<span data-ttu-id="e7cd5-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="e7cd5-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e7cd5-128">Implementations</span></span>

-   [<span data-ttu-id="e7cd5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7cd5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7cd5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7cd5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7cd5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e7cd5-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7cd5-134">Windows Server 2003</span></span>



| <span data-ttu-id="e7cd5-135">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-135">Entry</span></span> | <span data-ttu-id="e7cd5-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7cd5-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7cd5-139">System-Only</span></span>            | <span data-ttu-id="e7cd5-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-140">False</span></span>                             |
| <span data-ttu-id="e7cd5-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e7cd5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e7cd5-142">Vero</span><span class="sxs-lookup"><span data-stu-id="e7cd5-142">True</span></span>                              |
| <span data-ttu-id="e7cd5-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e7cd5-143">Is Indexed</span></span>             | <span data-ttu-id="e7cd5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-144">False</span></span>                             |
| <span data-ttu-id="e7cd5-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-145">In Global Catalog</span></span>      | <span data-ttu-id="e7cd5-146">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-146">False</span></span>                             |
| <span data-ttu-id="e7cd5-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7cd5-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e7cd5-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7cd5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7cd5-149">Range-Lower</span></span>            | <span data-ttu-id="e7cd5-150">1</span><span class="sxs-lookup"><span data-stu-id="e7cd5-150">1</span></span>                                 |
| <span data-ttu-id="e7cd5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7cd5-151">Range-Upper</span></span>            | <span data-ttu-id="e7cd5-152">256</span><span class="sxs-lookup"><span data-stu-id="e7cd5-152">256</span></span>                               |
| <span data-ttu-id="e7cd5-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-153">Search-Flags</span></span>           | <span data-ttu-id="e7cd5-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7cd5-154">0x00000000</span></span>                        |
| <span data-ttu-id="e7cd5-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-155">System-Flags</span></span>           | <span data-ttu-id="e7cd5-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7cd5-156">0x00000010</span></span>                        |
| <span data-ttu-id="e7cd5-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e7cd5-157">Classes used in</span></span>        | [<span data-ttu-id="e7cd5-158">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7cd5-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7cd5-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7cd5-160">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-160">Entry</span></span> | <span data-ttu-id="e7cd5-161">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7cd5-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7cd5-164">System-Only</span></span>            | <span data-ttu-id="e7cd5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-165">False</span></span>                             |
| <span data-ttu-id="e7cd5-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e7cd5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e7cd5-167">Vero</span><span class="sxs-lookup"><span data-stu-id="e7cd5-167">True</span></span>                              |
| <span data-ttu-id="e7cd5-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e7cd5-168">Is Indexed</span></span>             | <span data-ttu-id="e7cd5-169">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-169">False</span></span>                             |
| <span data-ttu-id="e7cd5-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-170">In Global Catalog</span></span>      | <span data-ttu-id="e7cd5-171">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-171">False</span></span>                             |
| <span data-ttu-id="e7cd5-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7cd5-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e7cd5-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7cd5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7cd5-174">Range-Lower</span></span>            | <span data-ttu-id="e7cd5-175">1</span><span class="sxs-lookup"><span data-stu-id="e7cd5-175">1</span></span>                                 |
| <span data-ttu-id="e7cd5-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7cd5-176">Range-Upper</span></span>            | <span data-ttu-id="e7cd5-177">256</span><span class="sxs-lookup"><span data-stu-id="e7cd5-177">256</span></span>                               |
| <span data-ttu-id="e7cd5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-178">Search-Flags</span></span>           | <span data-ttu-id="e7cd5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7cd5-179">0x00000000</span></span>                        |
| <span data-ttu-id="e7cd5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-180">System-Flags</span></span>           | <span data-ttu-id="e7cd5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7cd5-181">0x00000010</span></span>                        |
| <span data-ttu-id="e7cd5-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e7cd5-182">Classes used in</span></span>        | [<span data-ttu-id="e7cd5-183">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7cd5-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7cd5-184">Windows Server 2008</span></span>



| <span data-ttu-id="e7cd5-185">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-185">Entry</span></span> | <span data-ttu-id="e7cd5-186">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7cd5-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7cd5-189">System-Only</span></span>            | <span data-ttu-id="e7cd5-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-190">False</span></span>                             |
| <span data-ttu-id="e7cd5-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e7cd5-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e7cd5-192">Vero</span><span class="sxs-lookup"><span data-stu-id="e7cd5-192">True</span></span>                              |
| <span data-ttu-id="e7cd5-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e7cd5-193">Is Indexed</span></span>             | <span data-ttu-id="e7cd5-194">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-194">False</span></span>                             |
| <span data-ttu-id="e7cd5-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-195">In Global Catalog</span></span>      | <span data-ttu-id="e7cd5-196">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-196">False</span></span>                             |
| <span data-ttu-id="e7cd5-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7cd5-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e7cd5-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7cd5-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7cd5-199">Range-Lower</span></span>            | <span data-ttu-id="e7cd5-200">1</span><span class="sxs-lookup"><span data-stu-id="e7cd5-200">1</span></span>                                 |
| <span data-ttu-id="e7cd5-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7cd5-201">Range-Upper</span></span>            | <span data-ttu-id="e7cd5-202">256</span><span class="sxs-lookup"><span data-stu-id="e7cd5-202">256</span></span>                               |
| <span data-ttu-id="e7cd5-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-203">Search-Flags</span></span>           | <span data-ttu-id="e7cd5-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7cd5-204">0x00000000</span></span>                        |
| <span data-ttu-id="e7cd5-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-205">System-Flags</span></span>           | <span data-ttu-id="e7cd5-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7cd5-206">0x00000010</span></span>                        |
| <span data-ttu-id="e7cd5-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e7cd5-207">Classes used in</span></span>        | [<span data-ttu-id="e7cd5-208">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7cd5-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7cd5-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7cd5-210">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-210">Entry</span></span> | <span data-ttu-id="e7cd5-211">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7cd5-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7cd5-214">System-Only</span></span>            | <span data-ttu-id="e7cd5-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-215">False</span></span>                             |
| <span data-ttu-id="e7cd5-216">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e7cd5-216">Is-Single-Valued</span></span>       | <span data-ttu-id="e7cd5-217">Vero</span><span class="sxs-lookup"><span data-stu-id="e7cd5-217">True</span></span>                              |
| <span data-ttu-id="e7cd5-218">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e7cd5-218">Is Indexed</span></span>             | <span data-ttu-id="e7cd5-219">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-219">False</span></span>                             |
| <span data-ttu-id="e7cd5-220">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-220">In Global Catalog</span></span>      | <span data-ttu-id="e7cd5-221">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-221">False</span></span>                             |
| <span data-ttu-id="e7cd5-222">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7cd5-223">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e7cd5-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7cd5-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7cd5-224">Range-Lower</span></span>            | <span data-ttu-id="e7cd5-225">1</span><span class="sxs-lookup"><span data-stu-id="e7cd5-225">1</span></span>                                 |
| <span data-ttu-id="e7cd5-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7cd5-226">Range-Upper</span></span>            | <span data-ttu-id="e7cd5-227">256</span><span class="sxs-lookup"><span data-stu-id="e7cd5-227">256</span></span>                               |
| <span data-ttu-id="e7cd5-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-228">Search-Flags</span></span>           | <span data-ttu-id="e7cd5-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7cd5-229">0x00000000</span></span>                        |
| <span data-ttu-id="e7cd5-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-230">System-Flags</span></span>           | <span data-ttu-id="e7cd5-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7cd5-231">0x00000010</span></span>                        |
| <span data-ttu-id="e7cd5-232">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e7cd5-232">Classes used in</span></span>        | [<span data-ttu-id="e7cd5-233">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7cd5-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7cd5-234">Windows Server 2012</span></span>



| <span data-ttu-id="e7cd5-235">Voce</span><span class="sxs-lookup"><span data-stu-id="e7cd5-235">Entry</span></span> | <span data-ttu-id="e7cd5-236">Valore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7cd5-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e7cd5-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7cd5-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7cd5-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7cd5-239">System-Only</span></span>            | <span data-ttu-id="e7cd5-240">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-240">False</span></span>                             |
| <span data-ttu-id="e7cd5-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e7cd5-241">Is-Single-Valued</span></span>       | <span data-ttu-id="e7cd5-242">Vero</span><span class="sxs-lookup"><span data-stu-id="e7cd5-242">True</span></span>                              |
| <span data-ttu-id="e7cd5-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e7cd5-243">Is Indexed</span></span>             | <span data-ttu-id="e7cd5-244">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-244">False</span></span>                             |
| <span data-ttu-id="e7cd5-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e7cd5-245">In Global Catalog</span></span>      | <span data-ttu-id="e7cd5-246">Falso</span><span class="sxs-lookup"><span data-stu-id="e7cd5-246">False</span></span>                             |
| <span data-ttu-id="e7cd5-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e7cd5-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7cd5-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e7cd5-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7cd5-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7cd5-249">Range-Lower</span></span>            | <span data-ttu-id="e7cd5-250">1</span><span class="sxs-lookup"><span data-stu-id="e7cd5-250">1</span></span>                                 |
| <span data-ttu-id="e7cd5-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7cd5-251">Range-Upper</span></span>            | <span data-ttu-id="e7cd5-252">256</span><span class="sxs-lookup"><span data-stu-id="e7cd5-252">256</span></span>                               |
| <span data-ttu-id="e7cd5-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-253">Search-Flags</span></span>           | <span data-ttu-id="e7cd5-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7cd5-254">0x00000000</span></span>                        |
| <span data-ttu-id="e7cd5-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7cd5-255">System-Flags</span></span>           | <span data-ttu-id="e7cd5-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7cd5-256">0x00000010</span></span>                        |
| <span data-ttu-id="e7cd5-257">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e7cd5-257">Classes used in</span></span>        | [<span data-ttu-id="e7cd5-258">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e7cd5-258">**User**</span></span>](c-user.md)<br/> |



 

 





