---
title: Attributo Global-Address-List
description: Questo attributo viene utilizzato in un contenitore di Microsoft Exchange per archiviare il nome distinto di un elenco indirizzi globale (GAL) appena creato.
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Global-Address-List
- Schema AD dell'attributo globalAddressList
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302902"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="7217e-105">Attributo Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="7217e-105">Global-Address-List attribute</span></span>

<span data-ttu-id="7217e-106">Questo attributo viene utilizzato in un contenitore di Microsoft Exchange per archiviare il nome distinto di un elenco indirizzi globale (GAL) appena creato.</span><span class="sxs-lookup"><span data-stu-id="7217e-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="7217e-107">Questo attributo deve disporre di una voce prima che sia possibile abilitare i client di Messaging Application Programming Interface (MAPI) per l'utilizzo di un elenco indirizzi globale.</span><span class="sxs-lookup"><span data-stu-id="7217e-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="7217e-108">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-108">Entry</span></span> | <span data-ttu-id="7217e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7217e-110">CN</span><span class="sxs-lookup"><span data-stu-id="7217e-110">CN</span></span>                | <span data-ttu-id="7217e-111">Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="7217e-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="7217e-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7217e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7217e-113">globalAddressList</span><span class="sxs-lookup"><span data-stu-id="7217e-113">globalAddressList</span></span>                       |
| <span data-ttu-id="7217e-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7217e-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="7217e-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7217e-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7217e-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7217e-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7217e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-117">Attribute-Id</span></span>      | <span data-ttu-id="7217e-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="7217e-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="7217e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7217e-119">System-Id-Guid</span></span>    | <span data-ttu-id="7217e-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="7217e-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="7217e-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7217e-121">Syntax</span></span>            | [<span data-ttu-id="7217e-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7217e-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7217e-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7217e-123">Implementations</span></span>

-   [<span data-ttu-id="7217e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7217e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7217e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7217e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7217e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7217e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7217e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7217e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7217e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7217e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7217e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7217e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7217e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7217e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7217e-131">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-131">Entry</span></span> | <span data-ttu-id="7217e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-135">System-Only</span></span>            | <span data-ttu-id="7217e-136">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-136">False</span></span>                                                                                |
| <span data-ttu-id="7217e-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-138">False</span></span>                                                                                |
| <span data-ttu-id="7217e-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-139">Is Indexed</span></span>             | <span data-ttu-id="7217e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-140">False</span></span>                                                                                |
| <span data-ttu-id="7217e-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-141">In Global Catalog</span></span>      | <span data-ttu-id="7217e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-142">False</span></span>                                                                                |
| <span data-ttu-id="7217e-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-147">Search-Flags</span></span>           | <span data-ttu-id="7217e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-149">System-Flags</span></span>           | <span data-ttu-id="7217e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-151">Classes used in</span></span>        | [<span data-ttu-id="7217e-152">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7217e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7217e-153">Windows Server 2003</span></span>



| <span data-ttu-id="7217e-154">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-154">Entry</span></span> | <span data-ttu-id="7217e-155">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-158">System-Only</span></span>            | <span data-ttu-id="7217e-159">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-159">False</span></span>                                                                                |
| <span data-ttu-id="7217e-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-161">False</span></span>                                                                                |
| <span data-ttu-id="7217e-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-162">Is Indexed</span></span>             | <span data-ttu-id="7217e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-163">False</span></span>                                                                                |
| <span data-ttu-id="7217e-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-164">In Global Catalog</span></span>      | <span data-ttu-id="7217e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-165">False</span></span>                                                                                |
| <span data-ttu-id="7217e-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-170">Search-Flags</span></span>           | <span data-ttu-id="7217e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-172">System-Flags</span></span>           | <span data-ttu-id="7217e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-174">Classes used in</span></span>        | [<span data-ttu-id="7217e-175">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7217e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7217e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7217e-177">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-177">Entry</span></span> | <span data-ttu-id="7217e-178">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-181">System-Only</span></span>            | <span data-ttu-id="7217e-182">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-182">False</span></span>                                                                                |
| <span data-ttu-id="7217e-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-184">False</span></span>                                                                                |
| <span data-ttu-id="7217e-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-185">Is Indexed</span></span>             | <span data-ttu-id="7217e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-186">False</span></span>                                                                                |
| <span data-ttu-id="7217e-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-187">In Global Catalog</span></span>      | <span data-ttu-id="7217e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-188">False</span></span>                                                                                |
| <span data-ttu-id="7217e-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-193">Search-Flags</span></span>           | <span data-ttu-id="7217e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-195">System-Flags</span></span>           | <span data-ttu-id="7217e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-197">Classes used in</span></span>        | [<span data-ttu-id="7217e-198">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7217e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7217e-199">Windows Server 2008</span></span>



| <span data-ttu-id="7217e-200">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-200">Entry</span></span> | <span data-ttu-id="7217e-201">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-204">System-Only</span></span>            | <span data-ttu-id="7217e-205">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-205">False</span></span>                                                                                |
| <span data-ttu-id="7217e-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-207">False</span></span>                                                                                |
| <span data-ttu-id="7217e-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-208">Is Indexed</span></span>             | <span data-ttu-id="7217e-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-209">False</span></span>                                                                                |
| <span data-ttu-id="7217e-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-210">In Global Catalog</span></span>      | <span data-ttu-id="7217e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-211">False</span></span>                                                                                |
| <span data-ttu-id="7217e-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-216">Search-Flags</span></span>           | <span data-ttu-id="7217e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-218">System-Flags</span></span>           | <span data-ttu-id="7217e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-220">Classes used in</span></span>        | [<span data-ttu-id="7217e-221">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7217e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7217e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7217e-223">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-223">Entry</span></span> | <span data-ttu-id="7217e-224">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-227">System-Only</span></span>            | <span data-ttu-id="7217e-228">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-228">False</span></span>                                                                                |
| <span data-ttu-id="7217e-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-230">False</span></span>                                                                                |
| <span data-ttu-id="7217e-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-231">Is Indexed</span></span>             | <span data-ttu-id="7217e-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-232">False</span></span>                                                                                |
| <span data-ttu-id="7217e-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-233">In Global Catalog</span></span>      | <span data-ttu-id="7217e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-234">False</span></span>                                                                                |
| <span data-ttu-id="7217e-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-239">Search-Flags</span></span>           | <span data-ttu-id="7217e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-241">System-Flags</span></span>           | <span data-ttu-id="7217e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-243">Classes used in</span></span>        | [<span data-ttu-id="7217e-244">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7217e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7217e-245">Windows Server 2012</span></span>



| <span data-ttu-id="7217e-246">Voce</span><span class="sxs-lookup"><span data-stu-id="7217e-246">Entry</span></span> | <span data-ttu-id="7217e-247">Valore</span><span class="sxs-lookup"><span data-stu-id="7217e-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7217e-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7217e-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7217e-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="7217e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7217e-250">System-Only</span></span>            | <span data-ttu-id="7217e-251">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-251">False</span></span>                                                                                |
| <span data-ttu-id="7217e-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7217e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7217e-253">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-253">False</span></span>                                                                                |
| <span data-ttu-id="7217e-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7217e-254">Is Indexed</span></span>             | <span data-ttu-id="7217e-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-255">False</span></span>                                                                                |
| <span data-ttu-id="7217e-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7217e-256">In Global Catalog</span></span>      | <span data-ttu-id="7217e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7217e-257">False</span></span>                                                                                |
| <span data-ttu-id="7217e-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7217e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7217e-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7217e-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="7217e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7217e-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7217e-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="7217e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-262">Search-Flags</span></span>           | <span data-ttu-id="7217e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7217e-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="7217e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7217e-264">System-Flags</span></span>           | <span data-ttu-id="7217e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7217e-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="7217e-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7217e-266">Classes used in</span></span>        | [<span data-ttu-id="7217e-267">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="7217e-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





