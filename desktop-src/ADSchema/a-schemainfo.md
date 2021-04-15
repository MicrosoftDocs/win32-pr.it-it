---
title: Attributo Schema-Info
description: Valore binario interno utilizzato per rilevare le modifiche dello schema tra i controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC. Utilizzato per risolvere i vincoli quando viene sequestrato l'FSMO dello schema e viene apportata una modifica a più di un controller di dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema AD Schema-Info attribute
- Schema AD dell'attributo schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520022"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="cf0d2-106">Attributo Schema-Info</span><span class="sxs-lookup"><span data-stu-id="cf0d2-106">Schema-Info attribute</span></span>

<span data-ttu-id="cf0d2-107">Valore binario interno utilizzato per rilevare le modifiche dello schema tra i controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="cf0d2-108">Utilizzato per risolvere i vincoli quando viene sequestrato l'FSMO dello schema e viene apportata una modifica a più di un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="cf0d2-109">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-109">Entry</span></span> | <span data-ttu-id="cf0d2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="cf0d2-111">CN</span><span class="sxs-lookup"><span data-stu-id="cf0d2-111">CN</span></span>                | <span data-ttu-id="cf0d2-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="cf0d2-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="cf0d2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cf0d2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cf0d2-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="cf0d2-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cf0d2-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="cf0d2-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-116">Update Privilege</span></span>  | <span data-ttu-id="cf0d2-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="cf0d2-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="cf0d2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-119">Attribute-Id</span></span>      | <span data-ttu-id="cf0d2-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="cf0d2-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="cf0d2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cf0d2-121">System-Id-Guid</span></span>    | <span data-ttu-id="cf0d2-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cf0d2-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="cf0d2-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf0d2-123">Syntax</span></span>            | [<span data-ttu-id="cf0d2-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="cf0d2-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="cf0d2-125">Implementations</span></span>

-   [<span data-ttu-id="cf0d2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf0d2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf0d2-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cf0d2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf0d2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf0d2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf0d2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf0d2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf0d2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cf0d2-134">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-134">Entry</span></span> | <span data-ttu-id="cf0d2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-138">System-Only</span></span>            | <span data-ttu-id="cf0d2-139">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-139">True</span></span>                            |
| <span data-ttu-id="cf0d2-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-140">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-141">False</span></span>                           |
| <span data-ttu-id="cf0d2-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-142">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-143">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-143">False</span></span>                           |
| <span data-ttu-id="cf0d2-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-144">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-145">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-145">False</span></span>                           |
| <span data-ttu-id="cf0d2-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-150">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-151">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-152">System-Flags</span></span>           | <span data-ttu-id="cf0d2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-153">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-154">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf0d2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf0d2-156">Windows Server 2003</span></span>



| <span data-ttu-id="cf0d2-157">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-157">Entry</span></span> | <span data-ttu-id="cf0d2-158">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-161">System-Only</span></span>            | <span data-ttu-id="cf0d2-162">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-162">True</span></span>                            |
| <span data-ttu-id="cf0d2-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-164">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-164">False</span></span>                           |
| <span data-ttu-id="cf0d2-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-165">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-166">False</span></span>                           |
| <span data-ttu-id="cf0d2-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-167">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-168">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-168">False</span></span>                           |
| <span data-ttu-id="cf0d2-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-173">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-174">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-175">System-Flags</span></span>           | <span data-ttu-id="cf0d2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-176">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-177">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-178">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cf0d2-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="cf0d2-179">ADAM</span></span>



| <span data-ttu-id="cf0d2-180">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-180">Entry</span></span> | <span data-ttu-id="cf0d2-181">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-184">System-Only</span></span>            | <span data-ttu-id="cf0d2-185">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-185">True</span></span>                            |
| <span data-ttu-id="cf0d2-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-186">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-187">False</span></span>                           |
| <span data-ttu-id="cf0d2-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-188">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-189">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-189">False</span></span>                           |
| <span data-ttu-id="cf0d2-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-190">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-191">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-191">False</span></span>                           |
| <span data-ttu-id="cf0d2-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-196">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-197">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-198">System-Flags</span></span>           | <span data-ttu-id="cf0d2-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-199">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-200">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-201">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf0d2-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf0d2-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf0d2-203">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-203">Entry</span></span> | <span data-ttu-id="cf0d2-204">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-207">System-Only</span></span>            | <span data-ttu-id="cf0d2-208">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-208">True</span></span>                            |
| <span data-ttu-id="cf0d2-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-209">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-210">False</span></span>                           |
| <span data-ttu-id="cf0d2-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-211">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-212">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-212">False</span></span>                           |
| <span data-ttu-id="cf0d2-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-213">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-214">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-214">False</span></span>                           |
| <span data-ttu-id="cf0d2-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-219">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-220">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-221">System-Flags</span></span>           | <span data-ttu-id="cf0d2-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-222">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-223">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-224">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf0d2-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf0d2-225">Windows Server 2008</span></span>



| <span data-ttu-id="cf0d2-226">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-226">Entry</span></span> | <span data-ttu-id="cf0d2-227">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-230">System-Only</span></span>            | <span data-ttu-id="cf0d2-231">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-231">True</span></span>                            |
| <span data-ttu-id="cf0d2-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-232">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-233">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-233">False</span></span>                           |
| <span data-ttu-id="cf0d2-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-234">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-235">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-235">False</span></span>                           |
| <span data-ttu-id="cf0d2-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-236">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-237">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-237">False</span></span>                           |
| <span data-ttu-id="cf0d2-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-242">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-243">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-244">System-Flags</span></span>           | <span data-ttu-id="cf0d2-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-245">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-246">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-247">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf0d2-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf0d2-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf0d2-249">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-249">Entry</span></span> | <span data-ttu-id="cf0d2-250">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-253">System-Only</span></span>            | <span data-ttu-id="cf0d2-254">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-254">True</span></span>                            |
| <span data-ttu-id="cf0d2-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-255">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-256">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-256">False</span></span>                           |
| <span data-ttu-id="cf0d2-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-257">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-258">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-258">False</span></span>                           |
| <span data-ttu-id="cf0d2-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-259">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-260">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-260">False</span></span>                           |
| <span data-ttu-id="cf0d2-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-265">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-266">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-267">System-Flags</span></span>           | <span data-ttu-id="cf0d2-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-268">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-269">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-270">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf0d2-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf0d2-271">Windows Server 2012</span></span>



| <span data-ttu-id="cf0d2-272">Voce</span><span class="sxs-lookup"><span data-stu-id="cf0d2-272">Entry</span></span> | <span data-ttu-id="cf0d2-273">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0d2-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cf0d2-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0d2-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0d2-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0d2-276">System-Only</span></span>            | <span data-ttu-id="cf0d2-277">Vero</span><span class="sxs-lookup"><span data-stu-id="cf0d2-277">True</span></span>                            |
| <span data-ttu-id="cf0d2-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cf0d2-278">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0d2-279">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-279">False</span></span>                           |
| <span data-ttu-id="cf0d2-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cf0d2-280">Is Indexed</span></span>             | <span data-ttu-id="cf0d2-281">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-281">False</span></span>                           |
| <span data-ttu-id="cf0d2-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cf0d2-282">In Global Catalog</span></span>      | <span data-ttu-id="cf0d2-283">Falso</span><span class="sxs-lookup"><span data-stu-id="cf0d2-283">False</span></span>                           |
| <span data-ttu-id="cf0d2-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cf0d2-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0d2-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cf0d2-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0d2-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0d2-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0d2-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0d2-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-288">Search-Flags</span></span>           | <span data-ttu-id="cf0d2-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0d2-289">0x00000000</span></span>                      |
| <span data-ttu-id="cf0d2-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0d2-290">System-Flags</span></span>           | <span data-ttu-id="cf0d2-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0d2-291">0x00000010</span></span>                      |
| <span data-ttu-id="cf0d2-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cf0d2-292">Classes used in</span></span>        | [<span data-ttu-id="cf0d2-293">**DMD**</span><span class="sxs-lookup"><span data-stu-id="cf0d2-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





