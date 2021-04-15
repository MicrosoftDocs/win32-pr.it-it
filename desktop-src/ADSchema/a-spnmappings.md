---
title: Attributo SPN-Mappings
description: Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Schema AD SPN-Mappings attribute
- Schema AD dell'attributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519982"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="2e256-105">Attributo SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="2e256-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="2e256-106">Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN.</span><span class="sxs-lookup"><span data-stu-id="2e256-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="2e256-107">SPN è il nome usato da un client per identificare in modo univoco un'istanza di un servizio.</span><span class="sxs-lookup"><span data-stu-id="2e256-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="2e256-108">Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto.</span><span class="sxs-lookup"><span data-stu-id="2e256-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="2e256-109">Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN.</span><span class="sxs-lookup"><span data-stu-id="2e256-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="2e256-110">Ad esempio, "LDAP/..." È possibile eseguire il mapping degli SPN in modo che siano equivalenti a "host/..." SPN.</span><span class="sxs-lookup"><span data-stu-id="2e256-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="2e256-111">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-111">Entry</span></span> | <span data-ttu-id="2e256-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e256-113">CN</span><span class="sxs-lookup"><span data-stu-id="2e256-113">CN</span></span>                | <span data-ttu-id="2e256-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="2e256-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="2e256-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e256-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2e256-116">sPNMappings</span><span class="sxs-lookup"><span data-stu-id="2e256-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="2e256-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2e256-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="2e256-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e256-118">Update Privilege</span></span>  | <span data-ttu-id="2e256-119">Questo valore viene impostato durante l'installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2e256-119">This value is set during the product installation.</span></span> <span data-ttu-id="2e256-120">Può essere modificato dall'amministratore di sistema in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2e256-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="2e256-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e256-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="2e256-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-122">Attribute-Id</span></span>      | <span data-ttu-id="2e256-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="2e256-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="2e256-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e256-124">System-Id-Guid</span></span>    | <span data-ttu-id="2e256-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2e256-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="2e256-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e256-126">Syntax</span></span>            | [<span data-ttu-id="2e256-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2e256-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="2e256-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2e256-128">Implementations</span></span>

-   [<span data-ttu-id="2e256-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e256-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e256-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e256-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e256-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e256-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e256-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e256-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e256-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e256-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e256-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e256-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e256-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e256-135">Windows 2000 Server</span></span>



| <span data-ttu-id="2e256-136">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-136">Entry</span></span> | <span data-ttu-id="2e256-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-140">System-Only</span></span>            | <span data-ttu-id="2e256-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-141">False</span></span>                                            |
| <span data-ttu-id="2e256-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-143">False</span></span>                                            |
| <span data-ttu-id="2e256-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-144">Is Indexed</span></span>             | <span data-ttu-id="2e256-145">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-145">False</span></span>                                            |
| <span data-ttu-id="2e256-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-146">In Global Catalog</span></span>      | <span data-ttu-id="2e256-147">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-147">False</span></span>                                            |
| <span data-ttu-id="2e256-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-152">Search-Flags</span></span>           | <span data-ttu-id="2e256-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-153">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-154">System-Flags</span></span>           | <span data-ttu-id="2e256-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-155">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-156">Classes used in</span></span>        | [<span data-ttu-id="2e256-157">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e256-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e256-158">Windows Server 2003</span></span>



| <span data-ttu-id="2e256-159">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-159">Entry</span></span> | <span data-ttu-id="2e256-160">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-163">System-Only</span></span>            | <span data-ttu-id="2e256-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-164">False</span></span>                                            |
| <span data-ttu-id="2e256-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-166">False</span></span>                                            |
| <span data-ttu-id="2e256-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-167">Is Indexed</span></span>             | <span data-ttu-id="2e256-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-168">False</span></span>                                            |
| <span data-ttu-id="2e256-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-169">In Global Catalog</span></span>      | <span data-ttu-id="2e256-170">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-170">False</span></span>                                            |
| <span data-ttu-id="2e256-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-175">Search-Flags</span></span>           | <span data-ttu-id="2e256-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-176">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-177">System-Flags</span></span>           | <span data-ttu-id="2e256-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-178">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-179">Classes used in</span></span>        | [<span data-ttu-id="2e256-180">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e256-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e256-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e256-182">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-182">Entry</span></span> | <span data-ttu-id="2e256-183">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-186">System-Only</span></span>            | <span data-ttu-id="2e256-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-187">False</span></span>                                            |
| <span data-ttu-id="2e256-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-189">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-189">False</span></span>                                            |
| <span data-ttu-id="2e256-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-190">Is Indexed</span></span>             | <span data-ttu-id="2e256-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-191">False</span></span>                                            |
| <span data-ttu-id="2e256-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-192">In Global Catalog</span></span>      | <span data-ttu-id="2e256-193">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-193">False</span></span>                                            |
| <span data-ttu-id="2e256-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-198">Search-Flags</span></span>           | <span data-ttu-id="2e256-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-199">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-200">System-Flags</span></span>           | <span data-ttu-id="2e256-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-201">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-202">Classes used in</span></span>        | [<span data-ttu-id="2e256-203">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e256-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e256-204">Windows Server 2008</span></span>



| <span data-ttu-id="2e256-205">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-205">Entry</span></span> | <span data-ttu-id="2e256-206">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-209">System-Only</span></span>            | <span data-ttu-id="2e256-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-210">False</span></span>                                            |
| <span data-ttu-id="2e256-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-212">False</span></span>                                            |
| <span data-ttu-id="2e256-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-213">Is Indexed</span></span>             | <span data-ttu-id="2e256-214">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-214">False</span></span>                                            |
| <span data-ttu-id="2e256-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-215">In Global Catalog</span></span>      | <span data-ttu-id="2e256-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-216">False</span></span>                                            |
| <span data-ttu-id="2e256-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-221">Search-Flags</span></span>           | <span data-ttu-id="2e256-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-222">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-223">System-Flags</span></span>           | <span data-ttu-id="2e256-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-224">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-225">Classes used in</span></span>        | [<span data-ttu-id="2e256-226">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e256-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e256-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e256-228">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-228">Entry</span></span> | <span data-ttu-id="2e256-229">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-232">System-Only</span></span>            | <span data-ttu-id="2e256-233">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-233">False</span></span>                                            |
| <span data-ttu-id="2e256-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-235">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-235">False</span></span>                                            |
| <span data-ttu-id="2e256-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-236">Is Indexed</span></span>             | <span data-ttu-id="2e256-237">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-237">False</span></span>                                            |
| <span data-ttu-id="2e256-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-238">In Global Catalog</span></span>      | <span data-ttu-id="2e256-239">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-239">False</span></span>                                            |
| <span data-ttu-id="2e256-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-244">Search-Flags</span></span>           | <span data-ttu-id="2e256-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-245">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-246">System-Flags</span></span>           | <span data-ttu-id="2e256-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-247">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-248">Classes used in</span></span>        | [<span data-ttu-id="2e256-249">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e256-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e256-250">Windows Server 2012</span></span>



| <span data-ttu-id="2e256-251">Voce</span><span class="sxs-lookup"><span data-stu-id="2e256-251">Entry</span></span> | <span data-ttu-id="2e256-252">Valore</span><span class="sxs-lookup"><span data-stu-id="2e256-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2e256-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e256-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e256-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2e256-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e256-255">System-Only</span></span>            | <span data-ttu-id="2e256-256">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-256">False</span></span>                                            |
| <span data-ttu-id="2e256-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e256-257">Is-Single-Valued</span></span>       | <span data-ttu-id="2e256-258">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-258">False</span></span>                                            |
| <span data-ttu-id="2e256-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e256-259">Is Indexed</span></span>             | <span data-ttu-id="2e256-260">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-260">False</span></span>                                            |
| <span data-ttu-id="2e256-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e256-261">In Global Catalog</span></span>      | <span data-ttu-id="2e256-262">Falso</span><span class="sxs-lookup"><span data-stu-id="2e256-262">False</span></span>                                            |
| <span data-ttu-id="2e256-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e256-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e256-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e256-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2e256-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e256-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2e256-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e256-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2e256-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-267">Search-Flags</span></span>           | <span data-ttu-id="2e256-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e256-268">0x00000000</span></span>                                       |
| <span data-ttu-id="2e256-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e256-269">System-Flags</span></span>           | <span data-ttu-id="2e256-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e256-270">0x00000010</span></span>                                       |
| <span data-ttu-id="2e256-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e256-271">Classes used in</span></span>        | [<span data-ttu-id="2e256-272">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="2e256-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





