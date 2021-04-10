---
title: Attributo Product-Code
description: Questo attributo contiene un identificatore univoco per un'applicazione per una determinata versione del prodotto, rappresentata come GUID di stringa, ad esempio \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Schema AD Product-Code attribute
- Schema AD dell'attributo productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965072"
---
# <a name="product-code-attribute"></a><span data-ttu-id="a1b46-105">Attributo Product-Code</span><span class="sxs-lookup"><span data-stu-id="a1b46-105">Product-Code attribute</span></span>

<span data-ttu-id="a1b46-106">Questo attributo contiene un identificatore univoco per un'applicazione per una determinata versione del prodotto, rappresentata come GUID di stringa, ad esempio " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="a1b46-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="a1b46-107">Le lettere usate in questo GUID devono essere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="a1b46-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="a1b46-108">Questo ID deve variare per versioni e linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="a1b46-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="a1b46-109">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-109">Entry</span></span> | <span data-ttu-id="a1b46-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a1b46-111">CN</span><span class="sxs-lookup"><span data-stu-id="a1b46-111">CN</span></span>                | <span data-ttu-id="a1b46-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="a1b46-112">Product-Code</span></span>                                          |
| <span data-ttu-id="a1b46-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1b46-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a1b46-114">productCode</span><span class="sxs-lookup"><span data-stu-id="a1b46-114">productCode</span></span>                                           |
| <span data-ttu-id="a1b46-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a1b46-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a1b46-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a1b46-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a1b46-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-118">Attribute-Id</span></span>      | <span data-ttu-id="a1b46-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="a1b46-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="a1b46-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1b46-120">System-Id-Guid</span></span>    | <span data-ttu-id="a1b46-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a1b46-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="a1b46-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1b46-122">Syntax</span></span>            | [<span data-ttu-id="a1b46-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a1b46-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a1b46-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a1b46-124">Implementations</span></span>

-   [<span data-ttu-id="a1b46-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1b46-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1b46-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1b46-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1b46-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1b46-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1b46-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1b46-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1b46-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1b46-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1b46-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1b46-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1b46-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1b46-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a1b46-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-132">Entry</span></span> | <span data-ttu-id="a1b46-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-136">System-Only</span></span>            | <span data-ttu-id="a1b46-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-137">False</span></span>                                                            |
| <span data-ttu-id="a1b46-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-139">True</span></span>                                                             |
| <span data-ttu-id="a1b46-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-140">Is Indexed</span></span>             | <span data-ttu-id="a1b46-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-141">False</span></span>                                                            |
| <span data-ttu-id="a1b46-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-142">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-143">False</span></span>                                                            |
| <span data-ttu-id="a1b46-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-146">Range-Lower</span></span>            | <span data-ttu-id="a1b46-147">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-147">0</span></span>                                                                |
| <span data-ttu-id="a1b46-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-148">Range-Upper</span></span>            | <span data-ttu-id="a1b46-149">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-149">16</span></span>                                                               |
| <span data-ttu-id="a1b46-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-150">Search-Flags</span></span>           | <span data-ttu-id="a1b46-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-152">System-Flags</span></span>           | <span data-ttu-id="a1b46-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-154">Classes used in</span></span>        | [<span data-ttu-id="a1b46-155">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1b46-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1b46-156">Windows Server 2003</span></span>



| <span data-ttu-id="a1b46-157">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-157">Entry</span></span> | <span data-ttu-id="a1b46-158">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-161">System-Only</span></span>            | <span data-ttu-id="a1b46-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-162">False</span></span>                                                            |
| <span data-ttu-id="a1b46-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-164">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-164">True</span></span>                                                             |
| <span data-ttu-id="a1b46-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-165">Is Indexed</span></span>             | <span data-ttu-id="a1b46-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-166">False</span></span>                                                            |
| <span data-ttu-id="a1b46-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-167">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-168">False</span></span>                                                            |
| <span data-ttu-id="a1b46-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-171">Range-Lower</span></span>            | <span data-ttu-id="a1b46-172">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-172">0</span></span>                                                                |
| <span data-ttu-id="a1b46-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-173">Range-Upper</span></span>            | <span data-ttu-id="a1b46-174">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-174">16</span></span>                                                               |
| <span data-ttu-id="a1b46-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-175">Search-Flags</span></span>           | <span data-ttu-id="a1b46-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-177">System-Flags</span></span>           | <span data-ttu-id="a1b46-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-179">Classes used in</span></span>        | [<span data-ttu-id="a1b46-180">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1b46-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1b46-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1b46-182">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-182">Entry</span></span> | <span data-ttu-id="a1b46-183">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-186">System-Only</span></span>            | <span data-ttu-id="a1b46-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-187">False</span></span>                                                            |
| <span data-ttu-id="a1b46-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-189">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-189">True</span></span>                                                             |
| <span data-ttu-id="a1b46-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-190">Is Indexed</span></span>             | <span data-ttu-id="a1b46-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-191">False</span></span>                                                            |
| <span data-ttu-id="a1b46-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-192">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-193">False</span></span>                                                            |
| <span data-ttu-id="a1b46-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-196">Range-Lower</span></span>            | <span data-ttu-id="a1b46-197">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-197">0</span></span>                                                                |
| <span data-ttu-id="a1b46-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-198">Range-Upper</span></span>            | <span data-ttu-id="a1b46-199">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-199">16</span></span>                                                               |
| <span data-ttu-id="a1b46-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-200">Search-Flags</span></span>           | <span data-ttu-id="a1b46-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-202">System-Flags</span></span>           | <span data-ttu-id="a1b46-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-204">Classes used in</span></span>        | [<span data-ttu-id="a1b46-205">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1b46-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1b46-206">Windows Server 2008</span></span>



| <span data-ttu-id="a1b46-207">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-207">Entry</span></span> | <span data-ttu-id="a1b46-208">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-211">System-Only</span></span>            | <span data-ttu-id="a1b46-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-212">False</span></span>                                                            |
| <span data-ttu-id="a1b46-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-214">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-214">True</span></span>                                                             |
| <span data-ttu-id="a1b46-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-215">Is Indexed</span></span>             | <span data-ttu-id="a1b46-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-216">False</span></span>                                                            |
| <span data-ttu-id="a1b46-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-217">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-218">False</span></span>                                                            |
| <span data-ttu-id="a1b46-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-221">Range-Lower</span></span>            | <span data-ttu-id="a1b46-222">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-222">0</span></span>                                                                |
| <span data-ttu-id="a1b46-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-223">Range-Upper</span></span>            | <span data-ttu-id="a1b46-224">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-224">16</span></span>                                                               |
| <span data-ttu-id="a1b46-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-225">Search-Flags</span></span>           | <span data-ttu-id="a1b46-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-227">System-Flags</span></span>           | <span data-ttu-id="a1b46-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-229">Classes used in</span></span>        | [<span data-ttu-id="a1b46-230">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1b46-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1b46-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1b46-232">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-232">Entry</span></span> | <span data-ttu-id="a1b46-233">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-236">System-Only</span></span>            | <span data-ttu-id="a1b46-237">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-237">False</span></span>                                                            |
| <span data-ttu-id="a1b46-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-239">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-239">True</span></span>                                                             |
| <span data-ttu-id="a1b46-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-240">Is Indexed</span></span>             | <span data-ttu-id="a1b46-241">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-241">False</span></span>                                                            |
| <span data-ttu-id="a1b46-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-242">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-243">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-243">False</span></span>                                                            |
| <span data-ttu-id="a1b46-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-246">Range-Lower</span></span>            | <span data-ttu-id="a1b46-247">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-247">0</span></span>                                                                |
| <span data-ttu-id="a1b46-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-248">Range-Upper</span></span>            | <span data-ttu-id="a1b46-249">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-249">16</span></span>                                                               |
| <span data-ttu-id="a1b46-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-250">Search-Flags</span></span>           | <span data-ttu-id="a1b46-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-252">System-Flags</span></span>           | <span data-ttu-id="a1b46-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-254">Classes used in</span></span>        | [<span data-ttu-id="a1b46-255">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1b46-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1b46-256">Windows Server 2012</span></span>



| <span data-ttu-id="a1b46-257">Voce</span><span class="sxs-lookup"><span data-stu-id="a1b46-257">Entry</span></span> | <span data-ttu-id="a1b46-258">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b46-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a1b46-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a1b46-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1b46-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a1b46-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1b46-261">System-Only</span></span>            | <span data-ttu-id="a1b46-262">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-262">False</span></span>                                                            |
| <span data-ttu-id="a1b46-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a1b46-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a1b46-264">Vero</span><span class="sxs-lookup"><span data-stu-id="a1b46-264">True</span></span>                                                             |
| <span data-ttu-id="a1b46-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a1b46-265">Is Indexed</span></span>             | <span data-ttu-id="a1b46-266">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-266">False</span></span>                                                            |
| <span data-ttu-id="a1b46-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a1b46-267">In Global Catalog</span></span>      | <span data-ttu-id="a1b46-268">Falso</span><span class="sxs-lookup"><span data-stu-id="a1b46-268">False</span></span>                                                            |
| <span data-ttu-id="a1b46-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a1b46-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1b46-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a1b46-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a1b46-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1b46-271">Range-Lower</span></span>            | <span data-ttu-id="a1b46-272">0</span><span class="sxs-lookup"><span data-stu-id="a1b46-272">0</span></span>                                                                |
| <span data-ttu-id="a1b46-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1b46-273">Range-Upper</span></span>            | <span data-ttu-id="a1b46-274">16</span><span class="sxs-lookup"><span data-stu-id="a1b46-274">16</span></span>                                                               |
| <span data-ttu-id="a1b46-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-275">Search-Flags</span></span>           | <span data-ttu-id="a1b46-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1b46-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="a1b46-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1b46-277">System-Flags</span></span>           | <span data-ttu-id="a1b46-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1b46-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="a1b46-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a1b46-279">Classes used in</span></span>        | [<span data-ttu-id="a1b46-280">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="a1b46-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





