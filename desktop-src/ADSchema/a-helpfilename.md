---
title: Help-nome-file-attributo
description: Questo attributo è stato usato per Exchange 4,0. Contiene il nome che deve essere usato per il file quando il provider Scarica i dati della Guida in un computer client. Non viene usato per altre versioni di Exchange.
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- Guida-nome-file-schema AD
- Schema AD dell'attributo helpFileName
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875470"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="6183b-107">Help-nome-file-attributo</span><span class="sxs-lookup"><span data-stu-id="6183b-107">Help-File-Name attribute</span></span>

<span data-ttu-id="6183b-108">Questo attributo è stato usato per Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="6183b-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="6183b-109">Contiene il nome che deve essere usato per il file quando il provider Scarica i dati della Guida in un computer client.</span><span class="sxs-lookup"><span data-stu-id="6183b-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="6183b-110">Non viene usato per altre versioni di Exchange.</span><span class="sxs-lookup"><span data-stu-id="6183b-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="6183b-111">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-111">Entry</span></span> | <span data-ttu-id="6183b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6183b-113">CN</span><span class="sxs-lookup"><span data-stu-id="6183b-113">CN</span></span>                | <span data-ttu-id="6183b-114">Help-nome-file</span><span class="sxs-lookup"><span data-stu-id="6183b-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="6183b-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6183b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6183b-116">helpFileName</span><span class="sxs-lookup"><span data-stu-id="6183b-116">helpFileName</span></span>                                |
| <span data-ttu-id="6183b-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6183b-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="6183b-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6183b-118">Update Privilege</span></span>  | <span data-ttu-id="6183b-119">Viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6183b-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="6183b-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6183b-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6183b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-121">Attribute-Id</span></span>      | <span data-ttu-id="6183b-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="6183b-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="6183b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6183b-123">System-Id-Guid</span></span>    | <span data-ttu-id="6183b-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="6183b-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="6183b-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6183b-125">Syntax</span></span>            | [<span data-ttu-id="6183b-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6183b-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6183b-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6183b-127">Implementations</span></span>

-   [<span data-ttu-id="6183b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6183b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6183b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6183b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6183b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6183b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6183b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6183b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6183b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6183b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6183b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6183b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6183b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6183b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6183b-135">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-135">Entry</span></span> | <span data-ttu-id="6183b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-138">MAPI-Id</span></span>                | <span data-ttu-id="6183b-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-139">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-140">System-Only</span></span>            | <span data-ttu-id="6183b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-141">False</span></span>                                                    |
| <span data-ttu-id="6183b-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-143">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-143">True</span></span>                                                     |
| <span data-ttu-id="6183b-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-144">Is Indexed</span></span>             | <span data-ttu-id="6183b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-145">False</span></span>                                                    |
| <span data-ttu-id="6183b-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-146">In Global Catalog</span></span>      | <span data-ttu-id="6183b-147">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-147">False</span></span>                                                    |
| <span data-ttu-id="6183b-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-150">Range-Lower</span></span>            | <span data-ttu-id="6183b-151">1</span><span class="sxs-lookup"><span data-stu-id="6183b-151">1</span></span>                                                        |
| <span data-ttu-id="6183b-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-152">Range-Upper</span></span>            | <span data-ttu-id="6183b-153">13</span><span class="sxs-lookup"><span data-stu-id="6183b-153">13</span></span>                                                       |
| <span data-ttu-id="6183b-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-154">Search-Flags</span></span>           | <span data-ttu-id="6183b-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-155">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-156">System-Flags</span></span>           | <span data-ttu-id="6183b-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-157">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-158">Classes used in</span></span>        | [<span data-ttu-id="6183b-159">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6183b-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6183b-160">Windows Server 2003</span></span>



| <span data-ttu-id="6183b-161">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-161">Entry</span></span> | <span data-ttu-id="6183b-162">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-164">MAPI-Id</span></span>                | <span data-ttu-id="6183b-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-165">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-166">System-Only</span></span>            | <span data-ttu-id="6183b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-167">False</span></span>                                                    |
| <span data-ttu-id="6183b-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-168">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-169">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-169">True</span></span>                                                     |
| <span data-ttu-id="6183b-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-170">Is Indexed</span></span>             | <span data-ttu-id="6183b-171">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-171">False</span></span>                                                    |
| <span data-ttu-id="6183b-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-172">In Global Catalog</span></span>      | <span data-ttu-id="6183b-173">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-173">False</span></span>                                                    |
| <span data-ttu-id="6183b-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-176">Range-Lower</span></span>            | <span data-ttu-id="6183b-177">1</span><span class="sxs-lookup"><span data-stu-id="6183b-177">1</span></span>                                                        |
| <span data-ttu-id="6183b-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-178">Range-Upper</span></span>            | <span data-ttu-id="6183b-179">13</span><span class="sxs-lookup"><span data-stu-id="6183b-179">13</span></span>                                                       |
| <span data-ttu-id="6183b-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-180">Search-Flags</span></span>           | <span data-ttu-id="6183b-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-181">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-182">System-Flags</span></span>           | <span data-ttu-id="6183b-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-183">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-184">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-184">Classes used in</span></span>        | [<span data-ttu-id="6183b-185">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6183b-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6183b-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6183b-187">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-187">Entry</span></span> | <span data-ttu-id="6183b-188">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-190">MAPI-Id</span></span>                | <span data-ttu-id="6183b-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-191">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-192">System-Only</span></span>            | <span data-ttu-id="6183b-193">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-193">False</span></span>                                                    |
| <span data-ttu-id="6183b-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-194">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-195">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-195">True</span></span>                                                     |
| <span data-ttu-id="6183b-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-196">Is Indexed</span></span>             | <span data-ttu-id="6183b-197">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-197">False</span></span>                                                    |
| <span data-ttu-id="6183b-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-198">In Global Catalog</span></span>      | <span data-ttu-id="6183b-199">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-199">False</span></span>                                                    |
| <span data-ttu-id="6183b-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-202">Range-Lower</span></span>            | <span data-ttu-id="6183b-203">1</span><span class="sxs-lookup"><span data-stu-id="6183b-203">1</span></span>                                                        |
| <span data-ttu-id="6183b-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-204">Range-Upper</span></span>            | <span data-ttu-id="6183b-205">13</span><span class="sxs-lookup"><span data-stu-id="6183b-205">13</span></span>                                                       |
| <span data-ttu-id="6183b-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-206">Search-Flags</span></span>           | <span data-ttu-id="6183b-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-207">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-208">System-Flags</span></span>           | <span data-ttu-id="6183b-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-209">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-210">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-210">Classes used in</span></span>        | [<span data-ttu-id="6183b-211">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6183b-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6183b-212">Windows Server 2008</span></span>



| <span data-ttu-id="6183b-213">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-213">Entry</span></span> | <span data-ttu-id="6183b-214">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-215">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-216">MAPI-Id</span></span>                | <span data-ttu-id="6183b-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-217">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-218">System-Only</span></span>            | <span data-ttu-id="6183b-219">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-219">False</span></span>                                                    |
| <span data-ttu-id="6183b-220">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-220">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-221">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-221">True</span></span>                                                     |
| <span data-ttu-id="6183b-222">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-222">Is Indexed</span></span>             | <span data-ttu-id="6183b-223">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-223">False</span></span>                                                    |
| <span data-ttu-id="6183b-224">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-224">In Global Catalog</span></span>      | <span data-ttu-id="6183b-225">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-225">False</span></span>                                                    |
| <span data-ttu-id="6183b-226">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-227">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-228">Range-Lower</span></span>            | <span data-ttu-id="6183b-229">1</span><span class="sxs-lookup"><span data-stu-id="6183b-229">1</span></span>                                                        |
| <span data-ttu-id="6183b-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-230">Range-Upper</span></span>            | <span data-ttu-id="6183b-231">13</span><span class="sxs-lookup"><span data-stu-id="6183b-231">13</span></span>                                                       |
| <span data-ttu-id="6183b-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-232">Search-Flags</span></span>           | <span data-ttu-id="6183b-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-233">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-234">System-Flags</span></span>           | <span data-ttu-id="6183b-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-235">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-236">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-236">Classes used in</span></span>        | [<span data-ttu-id="6183b-237">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6183b-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6183b-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6183b-239">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-239">Entry</span></span> | <span data-ttu-id="6183b-240">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-241">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-242">MAPI-Id</span></span>                | <span data-ttu-id="6183b-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-243">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-244">System-Only</span></span>            | <span data-ttu-id="6183b-245">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-245">False</span></span>                                                    |
| <span data-ttu-id="6183b-246">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-246">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-247">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-247">True</span></span>                                                     |
| <span data-ttu-id="6183b-248">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-248">Is Indexed</span></span>             | <span data-ttu-id="6183b-249">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-249">False</span></span>                                                    |
| <span data-ttu-id="6183b-250">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-250">In Global Catalog</span></span>      | <span data-ttu-id="6183b-251">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-251">False</span></span>                                                    |
| <span data-ttu-id="6183b-252">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-253">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-254">Range-Lower</span></span>            | <span data-ttu-id="6183b-255">1</span><span class="sxs-lookup"><span data-stu-id="6183b-255">1</span></span>                                                        |
| <span data-ttu-id="6183b-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-256">Range-Upper</span></span>            | <span data-ttu-id="6183b-257">13</span><span class="sxs-lookup"><span data-stu-id="6183b-257">13</span></span>                                                       |
| <span data-ttu-id="6183b-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-258">Search-Flags</span></span>           | <span data-ttu-id="6183b-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-259">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-260">System-Flags</span></span>           | <span data-ttu-id="6183b-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-261">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-262">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-262">Classes used in</span></span>        | [<span data-ttu-id="6183b-263">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6183b-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6183b-264">Windows Server 2012</span></span>



| <span data-ttu-id="6183b-265">Voce</span><span class="sxs-lookup"><span data-stu-id="6183b-265">Entry</span></span> | <span data-ttu-id="6183b-266">Valore</span><span class="sxs-lookup"><span data-stu-id="6183b-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6183b-267">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6183b-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6183b-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6183b-268">MAPI-Id</span></span>                | <span data-ttu-id="6183b-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="6183b-269">0x803B</span></span>                                                   |
| <span data-ttu-id="6183b-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="6183b-270">System-Only</span></span>            | <span data-ttu-id="6183b-271">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-271">False</span></span>                                                    |
| <span data-ttu-id="6183b-272">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6183b-272">Is-Single-Valued</span></span>       | <span data-ttu-id="6183b-273">Vero</span><span class="sxs-lookup"><span data-stu-id="6183b-273">True</span></span>                                                     |
| <span data-ttu-id="6183b-274">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6183b-274">Is Indexed</span></span>             | <span data-ttu-id="6183b-275">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-275">False</span></span>                                                    |
| <span data-ttu-id="6183b-276">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6183b-276">In Global Catalog</span></span>      | <span data-ttu-id="6183b-277">Falso</span><span class="sxs-lookup"><span data-stu-id="6183b-277">False</span></span>                                                    |
| <span data-ttu-id="6183b-278">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6183b-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="6183b-279">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6183b-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6183b-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6183b-280">Range-Lower</span></span>            | <span data-ttu-id="6183b-281">1</span><span class="sxs-lookup"><span data-stu-id="6183b-281">1</span></span>                                                        |
| <span data-ttu-id="6183b-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6183b-282">Range-Upper</span></span>            | <span data-ttu-id="6183b-283">13</span><span class="sxs-lookup"><span data-stu-id="6183b-283">13</span></span>                                                       |
| <span data-ttu-id="6183b-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-284">Search-Flags</span></span>           | <span data-ttu-id="6183b-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6183b-285">0x00000000</span></span>                                               |
| <span data-ttu-id="6183b-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6183b-286">System-Flags</span></span>           | <span data-ttu-id="6183b-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6183b-287">0x00000010</span></span>                                               |
| <span data-ttu-id="6183b-288">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6183b-288">Classes used in</span></span>        | [<span data-ttu-id="6183b-289">**Visualizzazione-modello**</span><span class="sxs-lookup"><span data-stu-id="6183b-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





