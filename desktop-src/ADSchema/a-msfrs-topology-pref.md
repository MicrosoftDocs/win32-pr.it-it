---
title: attributo ms-FRS-topologia-pref
description: L'attributo ms-FRS-topologia-pref viene usato per registrare le impostazioni di topologia NTFRS preferite.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-FRS-topologia-pref
- msFRS-topologia-schema AD dell'attributo pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744666"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="fa515-105">attributo ms-FRS-topologia-pref</span><span class="sxs-lookup"><span data-stu-id="fa515-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="fa515-106">L'attributo **MS-FRS-topologia-pref** viene usato per registrare le impostazioni di topologia NTFRS preferite.</span><span class="sxs-lookup"><span data-stu-id="fa515-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="fa515-107">Quando un membro FRS viene aggiunto o eliminato al set di repliche, viene fatto riferimento a questi attributi e vengono apportate modifiche alle connessioni tra il resto dei membri FRS nel set di repliche.</span><span class="sxs-lookup"><span data-stu-id="fa515-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="fa515-108">I valori validi per questo attributo sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa515-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="fa515-109">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-109">Value</span></span> | <span data-ttu-id="fa515-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa515-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="fa515-111">1</span><span class="sxs-lookup"><span data-stu-id="fa515-111">1</span></span>     | <span data-ttu-id="fa515-112">\_anello RSTOPOLOGYPREF \_ FRS</span><span class="sxs-lookup"><span data-stu-id="fa515-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="fa515-113">2</span><span class="sxs-lookup"><span data-stu-id="fa515-113">2</span></span>     | <span data-ttu-id="fa515-114">FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE</span><span class="sxs-lookup"><span data-stu-id="fa515-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="fa515-115">3</span><span class="sxs-lookup"><span data-stu-id="fa515-115">3</span></span>     | <span data-ttu-id="fa515-116">FRS \_ RSTOPOLOGYPREF \_ FULLMESH</span><span class="sxs-lookup"><span data-stu-id="fa515-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="fa515-117">4</span><span class="sxs-lookup"><span data-stu-id="fa515-117">4</span></span>     | <span data-ttu-id="fa515-118">\_RSTOPOLOGYPREF \_ personalizzato FRS</span><span class="sxs-lookup"><span data-stu-id="fa515-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="fa515-119">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-119">Entry</span></span> | <span data-ttu-id="fa515-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fa515-121">CN</span><span class="sxs-lookup"><span data-stu-id="fa515-121">CN</span></span>                | <span data-ttu-id="fa515-122">MS-FRS-topologia-pref</span><span class="sxs-lookup"><span data-stu-id="fa515-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="fa515-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fa515-123">Ldap-Display-Name</span></span> | <span data-ttu-id="fa515-124">msFRS-topologia-pref</span><span class="sxs-lookup"><span data-stu-id="fa515-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="fa515-125">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fa515-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="fa515-126">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fa515-126">Update Privilege</span></span>  | <span data-ttu-id="fa515-127">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="fa515-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="fa515-128">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fa515-128">Update Frequency</span></span>  | <span data-ttu-id="fa515-129">Quando viene creato il set di repliche o la topologia preferita viene modificata.</span><span class="sxs-lookup"><span data-stu-id="fa515-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="fa515-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-130">Attribute-Id</span></span>      | <span data-ttu-id="fa515-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="fa515-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="fa515-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fa515-132">System-Id-Guid</span></span>    | <span data-ttu-id="fa515-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="fa515-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="fa515-134">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa515-134">Syntax</span></span>            | [<span data-ttu-id="fa515-135">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fa515-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="fa515-136">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fa515-136">Implementations</span></span>

-   [<span data-ttu-id="fa515-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fa515-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fa515-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fa515-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fa515-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fa515-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fa515-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fa515-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fa515-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fa515-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fa515-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa515-142">Windows Server 2003</span></span>



| <span data-ttu-id="fa515-143">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-143">Entry</span></span> | <span data-ttu-id="fa515-144">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa515-145">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fa515-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa515-147">System-Only</span></span>            | <span data-ttu-id="fa515-148">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-148">False</span></span>                                                     |
| <span data-ttu-id="fa515-149">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fa515-149">Is-Single-Valued</span></span>       | <span data-ttu-id="fa515-150">Vero</span><span class="sxs-lookup"><span data-stu-id="fa515-150">True</span></span>                                                      |
| <span data-ttu-id="fa515-151">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fa515-151">Is Indexed</span></span>             | <span data-ttu-id="fa515-152">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-152">False</span></span>                                                     |
| <span data-ttu-id="fa515-153">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fa515-153">In Global Catalog</span></span>      | <span data-ttu-id="fa515-154">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-154">False</span></span>                                                     |
| <span data-ttu-id="fa515-155">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fa515-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa515-156">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fa515-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa515-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa515-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa515-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-159">Search-Flags</span></span>           | <span data-ttu-id="fa515-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-160">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-161">System-Flags</span></span>           | <span data-ttu-id="fa515-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-162">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-163">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fa515-163">Classes used in</span></span>        | [<span data-ttu-id="fa515-164">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="fa515-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fa515-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fa515-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fa515-166">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-166">Entry</span></span> | <span data-ttu-id="fa515-167">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa515-168">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fa515-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa515-170">System-Only</span></span>            | <span data-ttu-id="fa515-171">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-171">False</span></span>                                                     |
| <span data-ttu-id="fa515-172">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fa515-172">Is-Single-Valued</span></span>       | <span data-ttu-id="fa515-173">Vero</span><span class="sxs-lookup"><span data-stu-id="fa515-173">True</span></span>                                                      |
| <span data-ttu-id="fa515-174">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fa515-174">Is Indexed</span></span>             | <span data-ttu-id="fa515-175">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-175">False</span></span>                                                     |
| <span data-ttu-id="fa515-176">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fa515-176">In Global Catalog</span></span>      | <span data-ttu-id="fa515-177">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-177">False</span></span>                                                     |
| <span data-ttu-id="fa515-178">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fa515-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa515-179">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fa515-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa515-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa515-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa515-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-182">Search-Flags</span></span>           | <span data-ttu-id="fa515-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-183">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-184">System-Flags</span></span>           | <span data-ttu-id="fa515-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-185">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-186">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fa515-186">Classes used in</span></span>        | [<span data-ttu-id="fa515-187">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="fa515-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fa515-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa515-188">Windows Server 2008</span></span>



| <span data-ttu-id="fa515-189">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-189">Entry</span></span> | <span data-ttu-id="fa515-190">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa515-191">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fa515-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa515-193">System-Only</span></span>            | <span data-ttu-id="fa515-194">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-194">False</span></span>                                                     |
| <span data-ttu-id="fa515-195">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fa515-195">Is-Single-Valued</span></span>       | <span data-ttu-id="fa515-196">Vero</span><span class="sxs-lookup"><span data-stu-id="fa515-196">True</span></span>                                                      |
| <span data-ttu-id="fa515-197">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fa515-197">Is Indexed</span></span>             | <span data-ttu-id="fa515-198">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-198">False</span></span>                                                     |
| <span data-ttu-id="fa515-199">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fa515-199">In Global Catalog</span></span>      | <span data-ttu-id="fa515-200">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-200">False</span></span>                                                     |
| <span data-ttu-id="fa515-201">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fa515-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa515-202">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fa515-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa515-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa515-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa515-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-205">Search-Flags</span></span>           | <span data-ttu-id="fa515-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-206">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-207">System-Flags</span></span>           | <span data-ttu-id="fa515-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-208">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fa515-209">Classes used in</span></span>        | [<span data-ttu-id="fa515-210">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="fa515-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fa515-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa515-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fa515-212">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-212">Entry</span></span> | <span data-ttu-id="fa515-213">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa515-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fa515-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa515-216">System-Only</span></span>            | <span data-ttu-id="fa515-217">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-217">False</span></span>                                                     |
| <span data-ttu-id="fa515-218">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fa515-218">Is-Single-Valued</span></span>       | <span data-ttu-id="fa515-219">Vero</span><span class="sxs-lookup"><span data-stu-id="fa515-219">True</span></span>                                                      |
| <span data-ttu-id="fa515-220">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fa515-220">Is Indexed</span></span>             | <span data-ttu-id="fa515-221">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-221">False</span></span>                                                     |
| <span data-ttu-id="fa515-222">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fa515-222">In Global Catalog</span></span>      | <span data-ttu-id="fa515-223">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-223">False</span></span>                                                     |
| <span data-ttu-id="fa515-224">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fa515-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa515-225">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fa515-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa515-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa515-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa515-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-228">Search-Flags</span></span>           | <span data-ttu-id="fa515-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-229">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-230">System-Flags</span></span>           | <span data-ttu-id="fa515-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-231">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-232">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fa515-232">Classes used in</span></span>        | [<span data-ttu-id="fa515-233">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="fa515-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fa515-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa515-234">Windows Server 2012</span></span>



| <span data-ttu-id="fa515-235">Voce</span><span class="sxs-lookup"><span data-stu-id="fa515-235">Entry</span></span> | <span data-ttu-id="fa515-236">Valore</span><span class="sxs-lookup"><span data-stu-id="fa515-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa515-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fa515-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa515-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa515-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa515-239">System-Only</span></span>            | <span data-ttu-id="fa515-240">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-240">False</span></span>                                                     |
| <span data-ttu-id="fa515-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fa515-241">Is-Single-Valued</span></span>       | <span data-ttu-id="fa515-242">Vero</span><span class="sxs-lookup"><span data-stu-id="fa515-242">True</span></span>                                                      |
| <span data-ttu-id="fa515-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fa515-243">Is Indexed</span></span>             | <span data-ttu-id="fa515-244">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-244">False</span></span>                                                     |
| <span data-ttu-id="fa515-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fa515-245">In Global Catalog</span></span>      | <span data-ttu-id="fa515-246">Falso</span><span class="sxs-lookup"><span data-stu-id="fa515-246">False</span></span>                                                     |
| <span data-ttu-id="fa515-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fa515-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa515-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fa515-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa515-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa515-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa515-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="fa515-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-251">Search-Flags</span></span>           | <span data-ttu-id="fa515-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-252">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa515-253">System-Flags</span></span>           | <span data-ttu-id="fa515-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa515-254">0x00000000</span></span>                                                |
| <span data-ttu-id="fa515-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fa515-255">Classes used in</span></span>        | [<span data-ttu-id="fa515-256">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="fa515-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





