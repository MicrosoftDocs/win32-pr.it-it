---
title: attributo ms-DS-ExecuteScriptPassword
description: Utilizzato durante la ridenominazione del dominio. Questo valore non può essere scritto o letto tramite LDAP.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-ExecuteScriptPassword
- attributo msDS-ExecuteScriptPassword-schema AD
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303267"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="88c7d-106">attributo ms-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="88c7d-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="88c7d-107">Utilizzato durante la ridenominazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="88c7d-107">Used during domain rename.</span></span> <span data-ttu-id="88c7d-108">Questo valore non può essere scritto o letto tramite LDAP.</span><span class="sxs-lookup"><span data-stu-id="88c7d-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="88c7d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-109">Entry</span></span> | <span data-ttu-id="88c7d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="88c7d-111">CN</span><span class="sxs-lookup"><span data-stu-id="88c7d-111">CN</span></span>                | <span data-ttu-id="88c7d-112">ms-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="88c7d-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="88c7d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="88c7d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="88c7d-114">msDS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="88c7d-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="88c7d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="88c7d-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="88c7d-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-116">Update Privilege</span></span>  | <span data-ttu-id="88c7d-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="88c7d-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="88c7d-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="88c7d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-119">Attribute-Id</span></span>      | <span data-ttu-id="88c7d-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="88c7d-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="88c7d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88c7d-121">System-Id-Guid</span></span>    | <span data-ttu-id="88c7d-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="88c7d-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="88c7d-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88c7d-123">Syntax</span></span>            | [<span data-ttu-id="88c7d-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="88c7d-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="88c7d-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="88c7d-125">Implementations</span></span>

-   [<span data-ttu-id="88c7d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88c7d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88c7d-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="88c7d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="88c7d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88c7d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88c7d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88c7d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88c7d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88c7d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88c7d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88c7d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="88c7d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88c7d-132">Windows Server 2003</span></span>



| <span data-ttu-id="88c7d-133">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-133">Entry</span></span> | <span data-ttu-id="88c7d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="88c7d-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-137">System-Only</span></span>            | <span data-ttu-id="88c7d-138">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-138">True</span></span>                                                          |
| <span data-ttu-id="88c7d-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-140">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-140">True</span></span>                                                          |
| <span data-ttu-id="88c7d-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-141">Is Indexed</span></span>             | <span data-ttu-id="88c7d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-142">False</span></span>                                                         |
| <span data-ttu-id="88c7d-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-143">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-144">False</span></span>                                                         |
| <span data-ttu-id="88c7d-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="88c7d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-147">Range-Lower</span></span>            | <span data-ttu-id="88c7d-148">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-148">0</span></span>                                                             |
| <span data-ttu-id="88c7d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-149">Range-Upper</span></span>            | <span data-ttu-id="88c7d-150">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-150">64</span></span>                                                            |
| <span data-ttu-id="88c7d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-151">Search-Flags</span></span>           | <span data-ttu-id="88c7d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="88c7d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-153">System-Flags</span></span>           | <span data-ttu-id="88c7d-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="88c7d-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-155">Classes used in</span></span>        | [<span data-ttu-id="88c7d-156">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="88c7d-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="88c7d-157">ADAM</span></span>



| <span data-ttu-id="88c7d-158">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-158">Entry</span></span> | <span data-ttu-id="88c7d-159">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="88c7d-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-162">System-Only</span></span>            | <span data-ttu-id="88c7d-163">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-163">True</span></span>                                                          |
| <span data-ttu-id="88c7d-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-165">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-165">True</span></span>                                                          |
| <span data-ttu-id="88c7d-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-166">Is Indexed</span></span>             | <span data-ttu-id="88c7d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-167">False</span></span>                                                         |
| <span data-ttu-id="88c7d-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-168">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-169">False</span></span>                                                         |
| <span data-ttu-id="88c7d-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="88c7d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-172">Range-Lower</span></span>            | <span data-ttu-id="88c7d-173">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-173">0</span></span>                                                             |
| <span data-ttu-id="88c7d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-174">Range-Upper</span></span>            | <span data-ttu-id="88c7d-175">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-175">64</span></span>                                                            |
| <span data-ttu-id="88c7d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-176">Search-Flags</span></span>           | <span data-ttu-id="88c7d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="88c7d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-178">System-Flags</span></span>           | <span data-ttu-id="88c7d-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="88c7d-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-180">Classes used in</span></span>        | [<span data-ttu-id="88c7d-181">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88c7d-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88c7d-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88c7d-183">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-183">Entry</span></span> | <span data-ttu-id="88c7d-184">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="88c7d-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="88c7d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-187">System-Only</span></span>            | <span data-ttu-id="88c7d-188">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-188">True</span></span>                                                          |
| <span data-ttu-id="88c7d-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-190">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-190">True</span></span>                                                          |
| <span data-ttu-id="88c7d-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-191">Is Indexed</span></span>             | <span data-ttu-id="88c7d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-192">False</span></span>                                                         |
| <span data-ttu-id="88c7d-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-193">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-194">False</span></span>                                                         |
| <span data-ttu-id="88c7d-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="88c7d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-197">Range-Lower</span></span>            | <span data-ttu-id="88c7d-198">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-198">0</span></span>                                                             |
| <span data-ttu-id="88c7d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-199">Range-Upper</span></span>            | <span data-ttu-id="88c7d-200">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-200">64</span></span>                                                            |
| <span data-ttu-id="88c7d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-201">Search-Flags</span></span>           | <span data-ttu-id="88c7d-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="88c7d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-203">System-Flags</span></span>           | <span data-ttu-id="88c7d-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="88c7d-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-205">Classes used in</span></span>        | [<span data-ttu-id="88c7d-206">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88c7d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88c7d-207">Windows Server 2008</span></span>



| <span data-ttu-id="88c7d-208">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-208">Entry</span></span> | <span data-ttu-id="88c7d-209">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c7d-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-212">System-Only</span></span>            | <span data-ttu-id="88c7d-213">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-213">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-215">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-215">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-216">Is Indexed</span></span>             | <span data-ttu-id="88c7d-217">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-217">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-218">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-219">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-219">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="88c7d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-222">Range-Lower</span></span>            | <span data-ttu-id="88c7d-223">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-223">0</span></span>                                                                                                       |
| <span data-ttu-id="88c7d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-224">Range-Upper</span></span>            | <span data-ttu-id="88c7d-225">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-225">64</span></span>                                                                                                      |
| <span data-ttu-id="88c7d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-226">Search-Flags</span></span>           | <span data-ttu-id="88c7d-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="88c7d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-228">System-Flags</span></span>           | <span data-ttu-id="88c7d-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="88c7d-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-230">Classes used in</span></span>        | [<span data-ttu-id="88c7d-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c7d-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c7d-232">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88c7d-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88c7d-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88c7d-234">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-234">Entry</span></span> | <span data-ttu-id="88c7d-235">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c7d-236">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-238">System-Only</span></span>            | <span data-ttu-id="88c7d-239">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-239">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-240">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-240">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-241">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-241">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-242">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-242">Is Indexed</span></span>             | <span data-ttu-id="88c7d-243">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-243">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-244">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-244">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-245">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-245">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-246">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-247">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="88c7d-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-248">Range-Lower</span></span>            | <span data-ttu-id="88c7d-249">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-249">0</span></span>                                                                                                       |
| <span data-ttu-id="88c7d-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-250">Range-Upper</span></span>            | <span data-ttu-id="88c7d-251">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-251">64</span></span>                                                                                                      |
| <span data-ttu-id="88c7d-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-252">Search-Flags</span></span>           | <span data-ttu-id="88c7d-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="88c7d-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-254">System-Flags</span></span>           | <span data-ttu-id="88c7d-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="88c7d-256">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-256">Classes used in</span></span>        | [<span data-ttu-id="88c7d-257">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c7d-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c7d-258">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88c7d-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88c7d-259">Windows Server 2012</span></span>



| <span data-ttu-id="88c7d-260">Voce</span><span class="sxs-lookup"><span data-stu-id="88c7d-260">Entry</span></span> | <span data-ttu-id="88c7d-261">Valore</span><span class="sxs-lookup"><span data-stu-id="88c7d-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c7d-262">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="88c7d-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c7d-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="88c7d-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c7d-264">System-Only</span></span>            | <span data-ttu-id="88c7d-265">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-265">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-266">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="88c7d-266">Is-Single-Valued</span></span>       | <span data-ttu-id="88c7d-267">Vero</span><span class="sxs-lookup"><span data-stu-id="88c7d-267">True</span></span>                                                                                                    |
| <span data-ttu-id="88c7d-268">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="88c7d-268">Is Indexed</span></span>             | <span data-ttu-id="88c7d-269">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-269">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-270">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="88c7d-270">In Global Catalog</span></span>      | <span data-ttu-id="88c7d-271">Falso</span><span class="sxs-lookup"><span data-stu-id="88c7d-271">False</span></span>                                                                                                   |
| <span data-ttu-id="88c7d-272">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="88c7d-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c7d-273">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="88c7d-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="88c7d-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c7d-274">Range-Lower</span></span>            | <span data-ttu-id="88c7d-275">0</span><span class="sxs-lookup"><span data-stu-id="88c7d-275">0</span></span>                                                                                                       |
| <span data-ttu-id="88c7d-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c7d-276">Range-Upper</span></span>            | <span data-ttu-id="88c7d-277">64</span><span class="sxs-lookup"><span data-stu-id="88c7d-277">64</span></span>                                                                                                      |
| <span data-ttu-id="88c7d-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-278">Search-Flags</span></span>           | <span data-ttu-id="88c7d-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c7d-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="88c7d-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c7d-280">System-Flags</span></span>           | <span data-ttu-id="88c7d-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="88c7d-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="88c7d-282">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="88c7d-282">Classes used in</span></span>        | [<span data-ttu-id="88c7d-283">**Computer**</span><span class="sxs-lookup"><span data-stu-id="88c7d-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="88c7d-284">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="88c7d-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





