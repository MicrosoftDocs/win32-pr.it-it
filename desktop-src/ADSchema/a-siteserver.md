---
title: Attributo Site-Server
description: Server principale licenze per un determinato sito.
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- Schema AD Site-Server attribute
- Schema AD dell'attributo siteServer
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104225293"
---
# <a name="site-server-attribute"></a><span data-ttu-id="6f3a8-105">Attributo Site-Server</span><span class="sxs-lookup"><span data-stu-id="6f3a8-105">Site-Server attribute</span></span>

<span data-ttu-id="6f3a8-106">Server principale licenze per un determinato sito.</span><span class="sxs-lookup"><span data-stu-id="6f3a8-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="6f3a8-107">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-107">Entry</span></span> | <span data-ttu-id="6f3a8-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="6f3a8-109">CN</span><span class="sxs-lookup"><span data-stu-id="6f3a8-109">CN</span></span>                | <span data-ttu-id="6f3a8-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="6f3a8-110">Site-Server</span></span>                                  |
| <span data-ttu-id="6f3a8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6f3a8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6f3a8-112">siteServer</span><span class="sxs-lookup"><span data-stu-id="6f3a8-112">siteServer</span></span>                                   |
| <span data-ttu-id="6f3a8-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6f3a8-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="6f3a8-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-114">Update Privilege</span></span>  | <span data-ttu-id="6f3a8-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="6f3a8-115">Domain administrator</span></span>                         |
| <span data-ttu-id="6f3a8-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-116">Update Frequency</span></span>  | <span data-ttu-id="6f3a8-117">Ogni volta che è necessario modificare il sito di gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="6f3a8-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="6f3a8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-118">Attribute-Id</span></span>      | <span data-ttu-id="6f3a8-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="6f3a8-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="6f3a8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6f3a8-120">System-Id-Guid</span></span>    | <span data-ttu-id="6f3a8-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6f3a8-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="6f3a8-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f3a8-122">Syntax</span></span>            | [<span data-ttu-id="6f3a8-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="6f3a8-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6f3a8-124">Implementations</span></span>

-   [<span data-ttu-id="6f3a8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f3a8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f3a8-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6f3a8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f3a8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f3a8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f3a8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f3a8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f3a8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6f3a8-133">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-133">Entry</span></span> | <span data-ttu-id="6f3a8-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-137">System-Only</span></span>            | <span data-ttu-id="6f3a8-138">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-138">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-140">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-141">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-142">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-142">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-143">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-144">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-149">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-151">System-Flags</span></span>           | <span data-ttu-id="6f3a8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-153">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-154">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f3a8-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f3a8-155">Windows Server 2003</span></span>



| <span data-ttu-id="6f3a8-156">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-156">Entry</span></span> | <span data-ttu-id="6f3a8-157">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-160">System-Only</span></span>            | <span data-ttu-id="6f3a8-161">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-161">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-163">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-163">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-164">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-165">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-165">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-166">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-167">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-172">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-174">System-Flags</span></span>           | <span data-ttu-id="6f3a8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-176">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-177">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6f3a8-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="6f3a8-178">ADAM</span></span>



| <span data-ttu-id="6f3a8-179">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-179">Entry</span></span> | <span data-ttu-id="6f3a8-180">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6f3a8-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6f3a8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6f3a8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-183">System-Only</span></span>            | <span data-ttu-id="6f3a8-184">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-184">False</span></span>        |
| <span data-ttu-id="6f3a8-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-186">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-186">False</span></span>        |
| <span data-ttu-id="6f3a8-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-187">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-188">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-188">False</span></span>        |
| <span data-ttu-id="6f3a8-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-189">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-190">False</span></span>        |
| <span data-ttu-id="6f3a8-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6f3a8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6f3a8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6f3a8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-195">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-196">0x00000000</span></span>   |
| <span data-ttu-id="6f3a8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-197">System-Flags</span></span>           | <span data-ttu-id="6f3a8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-198">0x00000010</span></span>   |
| <span data-ttu-id="6f3a8-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f3a8-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f3a8-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f3a8-201">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-201">Entry</span></span> | <span data-ttu-id="6f3a8-202">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-205">System-Only</span></span>            | <span data-ttu-id="6f3a8-206">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-206">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-208">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-208">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-209">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-210">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-211">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-212">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-212">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-217">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-219">System-Flags</span></span>           | <span data-ttu-id="6f3a8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-221">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-222">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f3a8-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f3a8-223">Windows Server 2008</span></span>



| <span data-ttu-id="6f3a8-224">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-224">Entry</span></span> | <span data-ttu-id="6f3a8-225">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-228">System-Only</span></span>            | <span data-ttu-id="6f3a8-229">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-229">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-231">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-232">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-233">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-234">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-235">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-235">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-240">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-242">System-Flags</span></span>           | <span data-ttu-id="6f3a8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-244">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-245">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f3a8-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f3a8-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f3a8-247">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-247">Entry</span></span> | <span data-ttu-id="6f3a8-248">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-251">System-Only</span></span>            | <span data-ttu-id="6f3a8-252">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-252">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-254">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-254">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-255">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-256">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-257">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-258">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-258">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-263">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-265">System-Flags</span></span>           | <span data-ttu-id="6f3a8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-267">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-268">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f3a8-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f3a8-269">Windows Server 2012</span></span>



| <span data-ttu-id="6f3a8-270">Voce</span><span class="sxs-lookup"><span data-stu-id="6f3a8-270">Entry</span></span> | <span data-ttu-id="6f3a8-271">Valore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f3a8-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f3a8-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f3a8-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="6f3a8-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f3a8-274">System-Only</span></span>            | <span data-ttu-id="6f3a8-275">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-275">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f3a8-276">Is-Single-Valued</span></span>       | <span data-ttu-id="6f3a8-277">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-277">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f3a8-278">Is Indexed</span></span>             | <span data-ttu-id="6f3a8-279">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-279">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f3a8-280">In Global Catalog</span></span>      | <span data-ttu-id="6f3a8-281">Falso</span><span class="sxs-lookup"><span data-stu-id="6f3a8-281">False</span></span>                                                                 |
| <span data-ttu-id="6f3a8-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f3a8-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f3a8-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f3a8-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="6f3a8-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f3a8-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f3a8-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="6f3a8-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-286">Search-Flags</span></span>           | <span data-ttu-id="6f3a8-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f3a8-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="6f3a8-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f3a8-288">System-Flags</span></span>           | <span data-ttu-id="6f3a8-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f3a8-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="6f3a8-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f3a8-290">Classes used in</span></span>        | [<span data-ttu-id="6f3a8-291">**Licenze-sito-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6f3a8-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





