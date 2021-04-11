---
title: Attributo MSI-file-list
description: Questo attributo contiene un elenco dei file di Microsoft Installer, ad esempio il file MSI di base (MSI) e i file di trasformazione MST (con estensione MST).
ms.assetid: 259a13a2-bb34-49aa-862e-4159e887310c
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MSI-file-list
- Schema AD dell'attributo msiFileList
topic_type:
- apiref
api_name:
- Msi-File-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05608cdf443ab053549fde7db509ca79be08b3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122916"
---
# <a name="msi-file-list-attribute"></a><span data-ttu-id="58c47-105">Attributo MSI-file-list</span><span class="sxs-lookup"><span data-stu-id="58c47-105">Msi-File-List attribute</span></span>

<span data-ttu-id="58c47-106">Questo attributo contiene un elenco dei file di Microsoft Installer, ad esempio il file MSI di base (MSI) e i file di trasformazione MST (con estensione MST).</span><span class="sxs-lookup"><span data-stu-id="58c47-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="58c47-107">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-107">Entry</span></span> | <span data-ttu-id="58c47-108">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="58c47-109">CN</span><span class="sxs-lookup"><span data-stu-id="58c47-109">CN</span></span>                | <span data-ttu-id="58c47-110">Elenco file MSI</span><span class="sxs-lookup"><span data-stu-id="58c47-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="58c47-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="58c47-111">Ldap-Display-Name</span></span> | <span data-ttu-id="58c47-112">msiFileList</span><span class="sxs-lookup"><span data-stu-id="58c47-112">msiFileList</span></span>                                 |
| <span data-ttu-id="58c47-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="58c47-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="58c47-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58c47-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="58c47-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58c47-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="58c47-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-116">Attribute-Id</span></span>      | <span data-ttu-id="58c47-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="58c47-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="58c47-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="58c47-118">System-Id-Guid</span></span>    | <span data-ttu-id="58c47-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="58c47-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="58c47-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58c47-120">Syntax</span></span>            | [<span data-ttu-id="58c47-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="58c47-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="58c47-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="58c47-122">Implementations</span></span>

-   [<span data-ttu-id="58c47-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58c47-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58c47-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58c47-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58c47-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58c47-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58c47-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58c47-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58c47-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58c47-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58c47-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58c47-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58c47-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58c47-129">Windows 2000 Server</span></span>



| <span data-ttu-id="58c47-130">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-130">Entry</span></span> | <span data-ttu-id="58c47-131">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-134">System-Only</span></span>            | <span data-ttu-id="58c47-135">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-135">False</span></span>                                                            |
| <span data-ttu-id="58c47-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-136">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-137">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-137">False</span></span>                                                            |
| <span data-ttu-id="58c47-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-138">Is Indexed</span></span>             | <span data-ttu-id="58c47-139">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-139">False</span></span>                                                            |
| <span data-ttu-id="58c47-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-140">In Global Catalog</span></span>      | <span data-ttu-id="58c47-141">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-141">False</span></span>                                                            |
| <span data-ttu-id="58c47-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-146">Search-Flags</span></span>           | <span data-ttu-id="58c47-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-148">System-Flags</span></span>           | <span data-ttu-id="58c47-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-150">Classes used in</span></span>        | [<span data-ttu-id="58c47-151">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58c47-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58c47-152">Windows Server 2003</span></span>



| <span data-ttu-id="58c47-153">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-153">Entry</span></span> | <span data-ttu-id="58c47-154">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-157">System-Only</span></span>            | <span data-ttu-id="58c47-158">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-158">False</span></span>                                                            |
| <span data-ttu-id="58c47-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-159">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-160">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-160">False</span></span>                                                            |
| <span data-ttu-id="58c47-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-161">Is Indexed</span></span>             | <span data-ttu-id="58c47-162">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-162">False</span></span>                                                            |
| <span data-ttu-id="58c47-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-163">In Global Catalog</span></span>      | <span data-ttu-id="58c47-164">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-164">False</span></span>                                                            |
| <span data-ttu-id="58c47-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-169">Search-Flags</span></span>           | <span data-ttu-id="58c47-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-171">System-Flags</span></span>           | <span data-ttu-id="58c47-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-173">Classes used in</span></span>        | [<span data-ttu-id="58c47-174">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58c47-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58c47-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58c47-176">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-176">Entry</span></span> | <span data-ttu-id="58c47-177">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-180">System-Only</span></span>            | <span data-ttu-id="58c47-181">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-181">False</span></span>                                                            |
| <span data-ttu-id="58c47-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-182">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-183">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-183">False</span></span>                                                            |
| <span data-ttu-id="58c47-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-184">Is Indexed</span></span>             | <span data-ttu-id="58c47-185">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-185">False</span></span>                                                            |
| <span data-ttu-id="58c47-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-186">In Global Catalog</span></span>      | <span data-ttu-id="58c47-187">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-187">False</span></span>                                                            |
| <span data-ttu-id="58c47-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-192">Search-Flags</span></span>           | <span data-ttu-id="58c47-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-194">System-Flags</span></span>           | <span data-ttu-id="58c47-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-196">Classes used in</span></span>        | [<span data-ttu-id="58c47-197">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58c47-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58c47-198">Windows Server 2008</span></span>



| <span data-ttu-id="58c47-199">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-199">Entry</span></span> | <span data-ttu-id="58c47-200">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-203">System-Only</span></span>            | <span data-ttu-id="58c47-204">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-204">False</span></span>                                                            |
| <span data-ttu-id="58c47-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-205">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-206">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-206">False</span></span>                                                            |
| <span data-ttu-id="58c47-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-207">Is Indexed</span></span>             | <span data-ttu-id="58c47-208">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-208">False</span></span>                                                            |
| <span data-ttu-id="58c47-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-209">In Global Catalog</span></span>      | <span data-ttu-id="58c47-210">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-210">False</span></span>                                                            |
| <span data-ttu-id="58c47-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-215">Search-Flags</span></span>           | <span data-ttu-id="58c47-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-217">System-Flags</span></span>           | <span data-ttu-id="58c47-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-219">Classes used in</span></span>        | [<span data-ttu-id="58c47-220">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58c47-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58c47-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58c47-222">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-222">Entry</span></span> | <span data-ttu-id="58c47-223">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-226">System-Only</span></span>            | <span data-ttu-id="58c47-227">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-227">False</span></span>                                                            |
| <span data-ttu-id="58c47-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-228">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-229">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-229">False</span></span>                                                            |
| <span data-ttu-id="58c47-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-230">Is Indexed</span></span>             | <span data-ttu-id="58c47-231">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-231">False</span></span>                                                            |
| <span data-ttu-id="58c47-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-232">In Global Catalog</span></span>      | <span data-ttu-id="58c47-233">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-233">False</span></span>                                                            |
| <span data-ttu-id="58c47-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-238">Search-Flags</span></span>           | <span data-ttu-id="58c47-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-240">System-Flags</span></span>           | <span data-ttu-id="58c47-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-242">Classes used in</span></span>        | [<span data-ttu-id="58c47-243">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58c47-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58c47-244">Windows Server 2012</span></span>



| <span data-ttu-id="58c47-245">Voce</span><span class="sxs-lookup"><span data-stu-id="58c47-245">Entry</span></span> | <span data-ttu-id="58c47-246">Valore</span><span class="sxs-lookup"><span data-stu-id="58c47-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="58c47-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58c47-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58c47-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="58c47-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="58c47-249">System-Only</span></span>            | <span data-ttu-id="58c47-250">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-250">False</span></span>                                                            |
| <span data-ttu-id="58c47-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58c47-251">Is-Single-Valued</span></span>       | <span data-ttu-id="58c47-252">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-252">False</span></span>                                                            |
| <span data-ttu-id="58c47-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58c47-253">Is Indexed</span></span>             | <span data-ttu-id="58c47-254">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-254">False</span></span>                                                            |
| <span data-ttu-id="58c47-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58c47-255">In Global Catalog</span></span>      | <span data-ttu-id="58c47-256">Falso</span><span class="sxs-lookup"><span data-stu-id="58c47-256">False</span></span>                                                            |
| <span data-ttu-id="58c47-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58c47-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="58c47-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58c47-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="58c47-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58c47-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58c47-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="58c47-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-261">Search-Flags</span></span>           | <span data-ttu-id="58c47-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58c47-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="58c47-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58c47-263">System-Flags</span></span>           | <span data-ttu-id="58c47-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58c47-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="58c47-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58c47-265">Classes used in</span></span>        | [<span data-ttu-id="58c47-266">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="58c47-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





