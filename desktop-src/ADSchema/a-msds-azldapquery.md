---
title: attributo ms-DS-AZ-LDAP-query
description: Stringa che definisce la query LDAP (lunghezza massima 4096) che determina l'appartenenza di un oggetto utente al gruppo.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- ms-DS-AZ-LDAP-query attribute AD schema
- attributo msDS-AzLDAPQuery-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122546"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="0dcc9-105">attributo ms-DS-AZ-LDAP-query</span><span class="sxs-lookup"><span data-stu-id="0dcc9-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="0dcc9-106">Stringa che definisce la query LDAP (lunghezza massima 4096) che determina l'appartenenza di un oggetto utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="0dcc9-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="0dcc9-107">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-107">Entry</span></span> | <span data-ttu-id="0dcc9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0dcc9-109">CN</span><span class="sxs-lookup"><span data-stu-id="0dcc9-109">CN</span></span>                | <span data-ttu-id="0dcc9-110">ms-DS-AZ-LDAP-query</span><span class="sxs-lookup"><span data-stu-id="0dcc9-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="0dcc9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0dcc9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0dcc9-112">msDS-AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="0dcc9-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="0dcc9-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0dcc9-113">Size</span></span>              | <span data-ttu-id="0dcc9-114">4096 caratteri</span><span class="sxs-lookup"><span data-stu-id="0dcc9-114">4096 characters</span></span>                             |
| <span data-ttu-id="0dcc9-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-115">Update Privilege</span></span>  | <span data-ttu-id="0dcc9-116">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="0dcc9-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="0dcc9-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-117">Update Frequency</span></span>  | <span data-ttu-id="0dcc9-118">Durante l'inizializzazione o la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0dcc9-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="0dcc9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-119">Attribute-Id</span></span>      | <span data-ttu-id="0dcc9-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="0dcc9-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="0dcc9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0dcc9-121">System-Id-Guid</span></span>    | <span data-ttu-id="0dcc9-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="0dcc9-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="0dcc9-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dcc9-123">Syntax</span></span>            | [<span data-ttu-id="0dcc9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0dcc9-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0dcc9-125">Implementations</span></span>

-   [<span data-ttu-id="0dcc9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0dcc9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0dcc9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0dcc9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0dcc9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0dcc9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0dcc9-131">Windows Server 2003</span></span>



| <span data-ttu-id="0dcc9-132">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-132">Entry</span></span> | <span data-ttu-id="0dcc9-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="0dcc9-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dcc9-136">System-Only</span></span>            | <span data-ttu-id="0dcc9-137">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-137">False</span></span>                               |
| <span data-ttu-id="0dcc9-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0dcc9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0dcc9-139">Vero</span><span class="sxs-lookup"><span data-stu-id="0dcc9-139">True</span></span>                                |
| <span data-ttu-id="0dcc9-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0dcc9-140">Is Indexed</span></span>             | <span data-ttu-id="0dcc9-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-141">False</span></span>                               |
| <span data-ttu-id="0dcc9-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0dcc9-142">In Global Catalog</span></span>      | <span data-ttu-id="0dcc9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-143">False</span></span>                               |
| <span data-ttu-id="0dcc9-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dcc9-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0dcc9-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="0dcc9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dcc9-146">Range-Lower</span></span>            | <span data-ttu-id="0dcc9-147">0</span><span class="sxs-lookup"><span data-stu-id="0dcc9-147">0</span></span>                                   |
| <span data-ttu-id="0dcc9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dcc9-148">Range-Upper</span></span>            | <span data-ttu-id="0dcc9-149">4096</span><span class="sxs-lookup"><span data-stu-id="0dcc9-149">4096</span></span>                                |
| <span data-ttu-id="0dcc9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-150">Search-Flags</span></span>           | <span data-ttu-id="0dcc9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0dcc9-151">0x00000000</span></span>                          |
| <span data-ttu-id="0dcc9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-152">System-Flags</span></span>           | <span data-ttu-id="0dcc9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dcc9-153">0x00000010</span></span>                          |
| <span data-ttu-id="0dcc9-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0dcc9-154">Classes used in</span></span>        | [<span data-ttu-id="0dcc9-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0dcc9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0dcc9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0dcc9-157">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-157">Entry</span></span> | <span data-ttu-id="0dcc9-158">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="0dcc9-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dcc9-161">System-Only</span></span>            | <span data-ttu-id="0dcc9-162">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-162">False</span></span>                               |
| <span data-ttu-id="0dcc9-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0dcc9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0dcc9-164">Vero</span><span class="sxs-lookup"><span data-stu-id="0dcc9-164">True</span></span>                                |
| <span data-ttu-id="0dcc9-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0dcc9-165">Is Indexed</span></span>             | <span data-ttu-id="0dcc9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-166">False</span></span>                               |
| <span data-ttu-id="0dcc9-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0dcc9-167">In Global Catalog</span></span>      | <span data-ttu-id="0dcc9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-168">False</span></span>                               |
| <span data-ttu-id="0dcc9-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dcc9-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0dcc9-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="0dcc9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dcc9-171">Range-Lower</span></span>            | <span data-ttu-id="0dcc9-172">0</span><span class="sxs-lookup"><span data-stu-id="0dcc9-172">0</span></span>                                   |
| <span data-ttu-id="0dcc9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dcc9-173">Range-Upper</span></span>            | <span data-ttu-id="0dcc9-174">4096</span><span class="sxs-lookup"><span data-stu-id="0dcc9-174">4096</span></span>                                |
| <span data-ttu-id="0dcc9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-175">Search-Flags</span></span>           | <span data-ttu-id="0dcc9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0dcc9-176">0x00000000</span></span>                          |
| <span data-ttu-id="0dcc9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-177">System-Flags</span></span>           | <span data-ttu-id="0dcc9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dcc9-178">0x00000010</span></span>                          |
| <span data-ttu-id="0dcc9-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0dcc9-179">Classes used in</span></span>        | [<span data-ttu-id="0dcc9-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0dcc9-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dcc9-181">Windows Server 2008</span></span>



| <span data-ttu-id="0dcc9-182">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-182">Entry</span></span> | <span data-ttu-id="0dcc9-183">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="0dcc9-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dcc9-186">System-Only</span></span>            | <span data-ttu-id="0dcc9-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-187">False</span></span>                               |
| <span data-ttu-id="0dcc9-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0dcc9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0dcc9-189">Vero</span><span class="sxs-lookup"><span data-stu-id="0dcc9-189">True</span></span>                                |
| <span data-ttu-id="0dcc9-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0dcc9-190">Is Indexed</span></span>             | <span data-ttu-id="0dcc9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-191">False</span></span>                               |
| <span data-ttu-id="0dcc9-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0dcc9-192">In Global Catalog</span></span>      | <span data-ttu-id="0dcc9-193">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-193">False</span></span>                               |
| <span data-ttu-id="0dcc9-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dcc9-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0dcc9-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="0dcc9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dcc9-196">Range-Lower</span></span>            | <span data-ttu-id="0dcc9-197">0</span><span class="sxs-lookup"><span data-stu-id="0dcc9-197">0</span></span>                                   |
| <span data-ttu-id="0dcc9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dcc9-198">Range-Upper</span></span>            | <span data-ttu-id="0dcc9-199">4096</span><span class="sxs-lookup"><span data-stu-id="0dcc9-199">4096</span></span>                                |
| <span data-ttu-id="0dcc9-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-200">Search-Flags</span></span>           | <span data-ttu-id="0dcc9-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0dcc9-201">0x00000000</span></span>                          |
| <span data-ttu-id="0dcc9-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-202">System-Flags</span></span>           | <span data-ttu-id="0dcc9-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dcc9-203">0x00000010</span></span>                          |
| <span data-ttu-id="0dcc9-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0dcc9-204">Classes used in</span></span>        | [<span data-ttu-id="0dcc9-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0dcc9-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0dcc9-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0dcc9-207">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-207">Entry</span></span> | <span data-ttu-id="0dcc9-208">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="0dcc9-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dcc9-211">System-Only</span></span>            | <span data-ttu-id="0dcc9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-212">False</span></span>                               |
| <span data-ttu-id="0dcc9-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0dcc9-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0dcc9-214">Vero</span><span class="sxs-lookup"><span data-stu-id="0dcc9-214">True</span></span>                                |
| <span data-ttu-id="0dcc9-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0dcc9-215">Is Indexed</span></span>             | <span data-ttu-id="0dcc9-216">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-216">False</span></span>                               |
| <span data-ttu-id="0dcc9-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0dcc9-217">In Global Catalog</span></span>      | <span data-ttu-id="0dcc9-218">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-218">False</span></span>                               |
| <span data-ttu-id="0dcc9-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dcc9-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0dcc9-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="0dcc9-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dcc9-221">Range-Lower</span></span>            | <span data-ttu-id="0dcc9-222">0</span><span class="sxs-lookup"><span data-stu-id="0dcc9-222">0</span></span>                                   |
| <span data-ttu-id="0dcc9-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dcc9-223">Range-Upper</span></span>            | <span data-ttu-id="0dcc9-224">4096</span><span class="sxs-lookup"><span data-stu-id="0dcc9-224">4096</span></span>                                |
| <span data-ttu-id="0dcc9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-225">Search-Flags</span></span>           | <span data-ttu-id="0dcc9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0dcc9-226">0x00000000</span></span>                          |
| <span data-ttu-id="0dcc9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-227">System-Flags</span></span>           | <span data-ttu-id="0dcc9-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dcc9-228">0x00000010</span></span>                          |
| <span data-ttu-id="0dcc9-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0dcc9-229">Classes used in</span></span>        | [<span data-ttu-id="0dcc9-230">**Group**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0dcc9-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0dcc9-231">Windows Server 2012</span></span>



| <span data-ttu-id="0dcc9-232">Voce</span><span class="sxs-lookup"><span data-stu-id="0dcc9-232">Entry</span></span> | <span data-ttu-id="0dcc9-233">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="0dcc9-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0dcc9-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0dcc9-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="0dcc9-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="0dcc9-236">System-Only</span></span>            | <span data-ttu-id="0dcc9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-237">False</span></span>                               |
| <span data-ttu-id="0dcc9-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0dcc9-238">Is-Single-Valued</span></span>       | <span data-ttu-id="0dcc9-239">Vero</span><span class="sxs-lookup"><span data-stu-id="0dcc9-239">True</span></span>                                |
| <span data-ttu-id="0dcc9-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0dcc9-240">Is Indexed</span></span>             | <span data-ttu-id="0dcc9-241">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-241">False</span></span>                               |
| <span data-ttu-id="0dcc9-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0dcc9-242">In Global Catalog</span></span>      | <span data-ttu-id="0dcc9-243">Falso</span><span class="sxs-lookup"><span data-stu-id="0dcc9-243">False</span></span>                               |
| <span data-ttu-id="0dcc9-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0dcc9-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="0dcc9-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0dcc9-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="0dcc9-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0dcc9-246">Range-Lower</span></span>            | <span data-ttu-id="0dcc9-247">0</span><span class="sxs-lookup"><span data-stu-id="0dcc9-247">0</span></span>                                   |
| <span data-ttu-id="0dcc9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0dcc9-248">Range-Upper</span></span>            | <span data-ttu-id="0dcc9-249">4096</span><span class="sxs-lookup"><span data-stu-id="0dcc9-249">4096</span></span>                                |
| <span data-ttu-id="0dcc9-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-250">Search-Flags</span></span>           | <span data-ttu-id="0dcc9-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0dcc9-251">0x00000000</span></span>                          |
| <span data-ttu-id="0dcc9-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0dcc9-252">System-Flags</span></span>           | <span data-ttu-id="0dcc9-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0dcc9-253">0x00000010</span></span>                          |
| <span data-ttu-id="0dcc9-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0dcc9-254">Classes used in</span></span>        | [<span data-ttu-id="0dcc9-255">**Group**</span><span class="sxs-lookup"><span data-stu-id="0dcc9-255">**Group**</span></span>](c-group.md)<br/> |



 

 





