---
title: attributo ms-DS-is-domain-for
description: Collegamento all'indietro per MS-DS-has-Domain-NCs. Identifica i controller di dominio che contengono la partizione come dominio primario. | attributo ms-DS-is-domain-for
ms.assetid: ec63ddb4-c220-492b-92ce-e3da2069bcb8
ms.tgt_platform: multiple
keywords:
- ms-DS-is-Domain-per lo schema AD dell'attributo
- attributo msDS-IsDomainFor-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Is-Domain-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56529497eb8081f53310e26b834194cdcdc11bf5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321367"
---
# <a name="ms-ds-is-domain-for-attribute"></a><span data-ttu-id="64821-107">attributo ms-DS-is-domain-for</span><span class="sxs-lookup"><span data-stu-id="64821-107">ms-DS-Is-Domain-For attribute</span></span>

<span data-ttu-id="64821-108">Collegamento all'indietro per [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md).</span><span class="sxs-lookup"><span data-stu-id="64821-108">Backward link for [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md).</span></span> <span data-ttu-id="64821-109">Identifica i controller di dominio che contengono la partizione come dominio primario.</span><span class="sxs-lookup"><span data-stu-id="64821-109">Identifies which DCs hold that partition as their primary domain.</span></span>



| <span data-ttu-id="64821-110">Voce</span><span class="sxs-lookup"><span data-stu-id="64821-110">Entry</span></span> | <span data-ttu-id="64821-111">Valore</span><span class="sxs-lookup"><span data-stu-id="64821-111">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="64821-112">CN</span><span class="sxs-lookup"><span data-stu-id="64821-112">CN</span></span>                | <span data-ttu-id="64821-113">ms-DS-is-domain-for</span><span class="sxs-lookup"><span data-stu-id="64821-113">ms-DS-Is-Domain-For</span></span>                     |
| <span data-ttu-id="64821-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64821-114">Ldap-Display-Name</span></span> | <span data-ttu-id="64821-115">msDS-IsDomainFor</span><span class="sxs-lookup"><span data-stu-id="64821-115">msDS-IsDomainFor</span></span>                        |
| <span data-ttu-id="64821-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="64821-116">Size</span></span>              | \-                                      |
| <span data-ttu-id="64821-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="64821-117">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="64821-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="64821-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="64821-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64821-119">Attribute-Id</span></span>      | <span data-ttu-id="64821-120">1.2.840.113556.1.4.1933</span><span class="sxs-lookup"><span data-stu-id="64821-120">1.2.840.113556.1.4.1933</span></span>                 |
| <span data-ttu-id="64821-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64821-121">System-Id-Guid</span></span>    | <span data-ttu-id="64821-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span><span class="sxs-lookup"><span data-stu-id="64821-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span></span>    |
| <span data-ttu-id="64821-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64821-123">Syntax</span></span>            | [<span data-ttu-id="64821-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="64821-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="64821-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="64821-125">Implementations</span></span>

-   [<span data-ttu-id="64821-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64821-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64821-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64821-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64821-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64821-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="64821-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64821-129">Windows Server 2008</span></span>



| <span data-ttu-id="64821-130">Voce</span><span class="sxs-lookup"><span data-stu-id="64821-130">Entry</span></span> | <span data-ttu-id="64821-131">Valore</span><span class="sxs-lookup"><span data-stu-id="64821-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64821-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="64821-132">Link-Id</span></span>                | <span data-ttu-id="64821-133">2027</span><span class="sxs-lookup"><span data-stu-id="64821-133">2027</span></span>                            |
| <span data-ttu-id="64821-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64821-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64821-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="64821-135">System-Only</span></span>            | <span data-ttu-id="64821-136">Vero</span><span class="sxs-lookup"><span data-stu-id="64821-136">True</span></span>                            |
| <span data-ttu-id="64821-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="64821-137">Is-Single-Valued</span></span>       | <span data-ttu-id="64821-138">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-138">False</span></span>                           |
| <span data-ttu-id="64821-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="64821-139">Is Indexed</span></span>             | <span data-ttu-id="64821-140">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-140">False</span></span>                           |
| <span data-ttu-id="64821-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="64821-141">In Global Catalog</span></span>      | <span data-ttu-id="64821-142">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-142">False</span></span>                           |
| <span data-ttu-id="64821-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="64821-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="64821-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="64821-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64821-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64821-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64821-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64821-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64821-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-147">Search-Flags</span></span>           | <span data-ttu-id="64821-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64821-148">0x00000000</span></span>                      |
| <span data-ttu-id="64821-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-149">System-Flags</span></span>           | <span data-ttu-id="64821-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="64821-150">0x00000011</span></span>                      |
| <span data-ttu-id="64821-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="64821-151">Classes used in</span></span>        | [<span data-ttu-id="64821-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="64821-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64821-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64821-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64821-154">Voce</span><span class="sxs-lookup"><span data-stu-id="64821-154">Entry</span></span> | <span data-ttu-id="64821-155">Valore</span><span class="sxs-lookup"><span data-stu-id="64821-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64821-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="64821-156">Link-Id</span></span>                | <span data-ttu-id="64821-157">2027</span><span class="sxs-lookup"><span data-stu-id="64821-157">2027</span></span>                            |
| <span data-ttu-id="64821-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64821-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64821-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="64821-159">System-Only</span></span>            | <span data-ttu-id="64821-160">Vero</span><span class="sxs-lookup"><span data-stu-id="64821-160">True</span></span>                            |
| <span data-ttu-id="64821-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="64821-161">Is-Single-Valued</span></span>       | <span data-ttu-id="64821-162">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-162">False</span></span>                           |
| <span data-ttu-id="64821-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="64821-163">Is Indexed</span></span>             | <span data-ttu-id="64821-164">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-164">False</span></span>                           |
| <span data-ttu-id="64821-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="64821-165">In Global Catalog</span></span>      | <span data-ttu-id="64821-166">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-166">False</span></span>                           |
| <span data-ttu-id="64821-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="64821-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="64821-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="64821-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64821-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64821-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64821-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64821-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64821-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-171">Search-Flags</span></span>           | <span data-ttu-id="64821-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64821-172">0x00000000</span></span>                      |
| <span data-ttu-id="64821-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-173">System-Flags</span></span>           | <span data-ttu-id="64821-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="64821-174">0x00000011</span></span>                      |
| <span data-ttu-id="64821-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="64821-175">Classes used in</span></span>        | [<span data-ttu-id="64821-176">**In alto**</span><span class="sxs-lookup"><span data-stu-id="64821-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64821-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64821-177">Windows Server 2012</span></span>



| <span data-ttu-id="64821-178">Voce</span><span class="sxs-lookup"><span data-stu-id="64821-178">Entry</span></span> | <span data-ttu-id="64821-179">Valore</span><span class="sxs-lookup"><span data-stu-id="64821-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64821-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="64821-180">Link-Id</span></span>                | <span data-ttu-id="64821-181">2027</span><span class="sxs-lookup"><span data-stu-id="64821-181">2027</span></span>                            |
| <span data-ttu-id="64821-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64821-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64821-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="64821-183">System-Only</span></span>            | <span data-ttu-id="64821-184">Vero</span><span class="sxs-lookup"><span data-stu-id="64821-184">True</span></span>                            |
| <span data-ttu-id="64821-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="64821-185">Is-Single-Valued</span></span>       | <span data-ttu-id="64821-186">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-186">False</span></span>                           |
| <span data-ttu-id="64821-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="64821-187">Is Indexed</span></span>             | <span data-ttu-id="64821-188">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-188">False</span></span>                           |
| <span data-ttu-id="64821-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="64821-189">In Global Catalog</span></span>      | <span data-ttu-id="64821-190">Falso</span><span class="sxs-lookup"><span data-stu-id="64821-190">False</span></span>                           |
| <span data-ttu-id="64821-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="64821-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="64821-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="64821-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64821-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64821-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64821-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64821-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64821-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-195">Search-Flags</span></span>           | <span data-ttu-id="64821-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64821-196">0x00000000</span></span>                      |
| <span data-ttu-id="64821-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64821-197">System-Flags</span></span>           | <span data-ttu-id="64821-198">0x00000011</span><span class="sxs-lookup"><span data-stu-id="64821-198">0x00000011</span></span>                      |
| <span data-ttu-id="64821-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="64821-199">Classes used in</span></span>        | [<span data-ttu-id="64821-200">**In alto**</span><span class="sxs-lookup"><span data-stu-id="64821-200">**Top**</span></span>](c-top.md)<br/> |



 

 





