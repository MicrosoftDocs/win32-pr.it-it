---
title: Aggiornamento-attributo prodotto-codice
description: Questo attributo contiene il codice prodotto di altri pacchetti, ad esempio applicazioni, che possono essere aggiornati da questo pacchetto o che possono aggiornare questo pacchetto.
ms.assetid: bf0ab06a-88a6-45af-ac9f-ee0ce648e51b
ms.tgt_platform: multiple
keywords:
- Aggiornare lo schema di AD dell'attributo Product-code
- Schema AD dell'attributo upgradeProductCode
topic_type:
- apiref
api_name:
- Upgrade-Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33734ec62665d301568f5f4152b39c5fbf4f94a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303107"
---
# <a name="upgrade-product-code-attribute"></a><span data-ttu-id="1f7fa-105">Aggiornamento-attributo prodotto-codice</span><span class="sxs-lookup"><span data-stu-id="1f7fa-105">Upgrade-Product-Code attribute</span></span>

<span data-ttu-id="1f7fa-106">Questo attributo contiene il codice prodotto di altri pacchetti, ad esempio applicazioni, che possono essere aggiornati da questo pacchetto o che possono aggiornare questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1f7fa-106">This attribute contains the product code of other packages, such as applications, that can be upgraded by this package, or that can upgrade this package.</span></span>



| <span data-ttu-id="1f7fa-107">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-107">Entry</span></span> | <span data-ttu-id="1f7fa-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1f7fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="1f7fa-109">CN</span></span>                | <span data-ttu-id="1f7fa-110">Aggiornamento-codice prodotto</span><span class="sxs-lookup"><span data-stu-id="1f7fa-110">Upgrade-Product-Code</span></span>                                  |
| <span data-ttu-id="1f7fa-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1f7fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1f7fa-112">upgradeProductCode</span><span class="sxs-lookup"><span data-stu-id="1f7fa-112">upgradeProductCode</span></span>                                    |
| <span data-ttu-id="1f7fa-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1f7fa-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1f7fa-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="1f7fa-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="1f7fa-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-116">Attribute-Id</span></span>      | <span data-ttu-id="1f7fa-117">1.2.840.113556.1.4.813</span><span class="sxs-lookup"><span data-stu-id="1f7fa-117">1.2.840.113556.1.4.813</span></span>                                |
| <span data-ttu-id="1f7fa-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1f7fa-118">System-Id-Guid</span></span>    | <span data-ttu-id="1f7fa-119">d9e18312-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1f7fa-119">d9e18312-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="1f7fa-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f7fa-120">Syntax</span></span>            | [<span data-ttu-id="1f7fa-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1f7fa-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1f7fa-122">Implementations</span></span>

-   [<span data-ttu-id="1f7fa-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1f7fa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f7fa-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f7fa-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f7fa-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f7fa-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1f7fa-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f7fa-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1f7fa-130">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-130">Entry</span></span> | <span data-ttu-id="1f7fa-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-134">System-Only</span></span>            | <span data-ttu-id="1f7fa-135">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-135">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-137">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-138">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-139">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-139">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-140">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-141">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-144">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-145">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-145">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-146">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-147">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-147">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-148">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-149">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-150">System-Flags</span></span>           | <span data-ttu-id="1f7fa-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-151">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-152">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-153">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1f7fa-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f7fa-154">Windows Server 2003</span></span>



| <span data-ttu-id="1f7fa-155">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-155">Entry</span></span> | <span data-ttu-id="1f7fa-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-156">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-157">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-158">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-159">System-Only</span></span>            | <span data-ttu-id="1f7fa-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-160">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-162">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-162">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-163">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-164">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-165">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-166">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-168">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-169">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-170">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-170">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-171">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-172">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-172">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-173">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-174">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-175">System-Flags</span></span>           | <span data-ttu-id="1f7fa-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-176">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-177">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-178">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-178">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f7fa-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f7fa-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f7fa-180">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-180">Entry</span></span> | <span data-ttu-id="1f7fa-181">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-181">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-182">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-183">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-184">System-Only</span></span>            | <span data-ttu-id="1f7fa-185">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-185">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-187">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-188">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-189">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-190">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-191">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-191">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-193">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-194">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-195">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-195">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-196">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-197">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-197">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-198">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-199">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-200">System-Flags</span></span>           | <span data-ttu-id="1f7fa-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-201">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-202">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-203">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-203">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f7fa-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f7fa-204">Windows Server 2008</span></span>



| <span data-ttu-id="1f7fa-205">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-205">Entry</span></span> | <span data-ttu-id="1f7fa-206">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-206">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-207">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-208">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-209">System-Only</span></span>            | <span data-ttu-id="1f7fa-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-210">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-212">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-213">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-214">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-214">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-215">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-216">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-216">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-218">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-219">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-220">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-220">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-221">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-222">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-222">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-223">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-224">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-225">System-Flags</span></span>           | <span data-ttu-id="1f7fa-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-226">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-227">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-228">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-228">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f7fa-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f7fa-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f7fa-230">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-230">Entry</span></span> | <span data-ttu-id="1f7fa-231">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-231">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-232">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-233">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-234">System-Only</span></span>            | <span data-ttu-id="1f7fa-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-235">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-236">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-237">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-237">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-238">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-239">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-239">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-240">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-241">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-241">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-243">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-244">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-245">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-245">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-246">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-247">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-247">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-248">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-249">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-250">System-Flags</span></span>           | <span data-ttu-id="1f7fa-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-251">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-252">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-253">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-253">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f7fa-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f7fa-254">Windows Server 2012</span></span>



| <span data-ttu-id="1f7fa-255">Voce</span><span class="sxs-lookup"><span data-stu-id="1f7fa-255">Entry</span></span> | <span data-ttu-id="1f7fa-256">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-256">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f7fa-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f7fa-257">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f7fa-258">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f7fa-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f7fa-259">System-Only</span></span>            | <span data-ttu-id="1f7fa-260">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-260">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f7fa-261">Is-Single-Valued</span></span>       | <span data-ttu-id="1f7fa-262">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-262">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f7fa-263">Is Indexed</span></span>             | <span data-ttu-id="1f7fa-264">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-264">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f7fa-265">In Global Catalog</span></span>      | <span data-ttu-id="1f7fa-266">Falso</span><span class="sxs-lookup"><span data-stu-id="1f7fa-266">False</span></span>                                                            |
| <span data-ttu-id="1f7fa-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f7fa-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f7fa-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f7fa-268">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f7fa-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f7fa-269">Range-Lower</span></span>            | <span data-ttu-id="1f7fa-270">0</span><span class="sxs-lookup"><span data-stu-id="1f7fa-270">0</span></span>                                                                |
| <span data-ttu-id="1f7fa-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f7fa-271">Range-Upper</span></span>            | <span data-ttu-id="1f7fa-272">16</span><span class="sxs-lookup"><span data-stu-id="1f7fa-272">16</span></span>                                                               |
| <span data-ttu-id="1f7fa-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-273">Search-Flags</span></span>           | <span data-ttu-id="1f7fa-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f7fa-274">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f7fa-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f7fa-275">System-Flags</span></span>           | <span data-ttu-id="1f7fa-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f7fa-276">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f7fa-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f7fa-277">Classes used in</span></span>        | [<span data-ttu-id="1f7fa-278">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1f7fa-278">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





