---
title: Attributo User-Principal-Name
description: Questo attributo contiene l'UPN che è un nome di accesso Internet per un utente in base allo standard Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo nome-entità-utente
- Schema AD dell'attributo userPrincipalName
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965184"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="7f7af-105">Attributo User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="7f7af-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="7f7af-106">Questo attributo contiene l'UPN che è un nome di accesso Internet per un utente in base allo standard Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span><span class="sxs-lookup"><span data-stu-id="7f7af-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="7f7af-107">L'UPN è più breve del nome distinto e più facile da ricordare.</span><span class="sxs-lookup"><span data-stu-id="7f7af-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="7f7af-108">Per convenzione, deve essere mappato al nome di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7f7af-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="7f7af-109">Il valore impostato per questo attributo è uguale alla lunghezza dell'ID dell'utente e al nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="7f7af-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="7f7af-110">Per ulteriori informazioni su questo attributo, vedere la pagina relativa agli [attributi di denominazione utente](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="7f7af-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="7f7af-111">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-111">Entry</span></span> | <span data-ttu-id="7f7af-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7f7af-113">CN</span><span class="sxs-lookup"><span data-stu-id="7f7af-113">CN</span></span>                | <span data-ttu-id="7f7af-114">User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="7f7af-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="7f7af-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7f7af-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7f7af-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7f7af-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="7f7af-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7f7af-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="7f7af-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-118">Update Privilege</span></span>  | <span data-ttu-id="7f7af-119">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="7f7af-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="7f7af-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-120">Update Frequency</span></span>  | <span data-ttu-id="7f7af-121">In teoria, questo non dovrebbe mai cambiare.</span><span class="sxs-lookup"><span data-stu-id="7f7af-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="7f7af-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-122">Attribute-Id</span></span>      | <span data-ttu-id="7f7af-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="7f7af-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="7f7af-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7f7af-124">System-Id-Guid</span></span>    | <span data-ttu-id="7f7af-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7f7af-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="7f7af-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f7af-126">Syntax</span></span>            | [<span data-ttu-id="7f7af-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7f7af-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7f7af-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7f7af-128">Implementations</span></span>

-   [<span data-ttu-id="7f7af-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f7af-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f7af-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f7af-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f7af-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7f7af-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7f7af-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f7af-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f7af-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f7af-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f7af-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f7af-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f7af-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f7af-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f7af-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f7af-136">Windows 2000 Server</span></span>



| <span data-ttu-id="7f7af-137">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-137">Entry</span></span> | <span data-ttu-id="7f7af-138">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-141">System-Only</span></span>            | <span data-ttu-id="7f7af-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-142">False</span></span>                             |
| <span data-ttu-id="7f7af-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-143">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-144">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-144">True</span></span>                              |
| <span data-ttu-id="7f7af-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-145">Is Indexed</span></span>             | <span data-ttu-id="7f7af-146">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-146">True</span></span>                              |
| <span data-ttu-id="7f7af-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-147">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-148">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-148">True</span></span>                              |
| <span data-ttu-id="7f7af-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-153">Search-Flags</span></span>           | <span data-ttu-id="7f7af-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-154">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-155">System-Flags</span></span>           | <span data-ttu-id="7f7af-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-156">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-157">Classes used in</span></span>        | [<span data-ttu-id="7f7af-158">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f7af-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f7af-159">Windows Server 2003</span></span>



| <span data-ttu-id="7f7af-160">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-160">Entry</span></span> | <span data-ttu-id="7f7af-161">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-164">System-Only</span></span>            | <span data-ttu-id="7f7af-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-165">False</span></span>                             |
| <span data-ttu-id="7f7af-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-166">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-167">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-167">True</span></span>                              |
| <span data-ttu-id="7f7af-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-168">Is Indexed</span></span>             | <span data-ttu-id="7f7af-169">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-169">True</span></span>                              |
| <span data-ttu-id="7f7af-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-170">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-171">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-171">True</span></span>                              |
| <span data-ttu-id="7f7af-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-176">Search-Flags</span></span>           | <span data-ttu-id="7f7af-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-177">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-178">System-Flags</span></span>           | <span data-ttu-id="7f7af-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-179">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-180">Classes used in</span></span>        | [<span data-ttu-id="7f7af-181">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7f7af-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="7f7af-182">ADAM</span></span>



| <span data-ttu-id="7f7af-183">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-183">Entry</span></span> | <span data-ttu-id="7f7af-184">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="7f7af-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="7f7af-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="7f7af-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-187">System-Only</span></span>            | <span data-ttu-id="7f7af-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-188">False</span></span>        |
| <span data-ttu-id="7f7af-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-190">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-190">True</span></span>         |
| <span data-ttu-id="7f7af-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-191">Is Indexed</span></span>             | <span data-ttu-id="7f7af-192">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-192">True</span></span>         |
| <span data-ttu-id="7f7af-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-193">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-194">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-194">True</span></span>         |
| <span data-ttu-id="7f7af-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="7f7af-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="7f7af-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="7f7af-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-199">Search-Flags</span></span>           | <span data-ttu-id="7f7af-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-200">0x00000001</span></span>   |
| <span data-ttu-id="7f7af-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-201">System-Flags</span></span>           | <span data-ttu-id="7f7af-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-202">0x00000012</span></span>   |
| <span data-ttu-id="7f7af-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f7af-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f7af-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f7af-205">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-205">Entry</span></span> | <span data-ttu-id="7f7af-206">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-209">System-Only</span></span>            | <span data-ttu-id="7f7af-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-210">False</span></span>                             |
| <span data-ttu-id="7f7af-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-211">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-212">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-212">True</span></span>                              |
| <span data-ttu-id="7f7af-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-213">Is Indexed</span></span>             | <span data-ttu-id="7f7af-214">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-214">True</span></span>                              |
| <span data-ttu-id="7f7af-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-215">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-216">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-216">True</span></span>                              |
| <span data-ttu-id="7f7af-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-221">Search-Flags</span></span>           | <span data-ttu-id="7f7af-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-222">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-223">System-Flags</span></span>           | <span data-ttu-id="7f7af-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-224">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-225">Classes used in</span></span>        | [<span data-ttu-id="7f7af-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f7af-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f7af-227">Windows Server 2008</span></span>



| <span data-ttu-id="7f7af-228">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-228">Entry</span></span> | <span data-ttu-id="7f7af-229">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-232">System-Only</span></span>            | <span data-ttu-id="7f7af-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-233">False</span></span>                             |
| <span data-ttu-id="7f7af-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-235">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-235">True</span></span>                              |
| <span data-ttu-id="7f7af-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-236">Is Indexed</span></span>             | <span data-ttu-id="7f7af-237">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-237">True</span></span>                              |
| <span data-ttu-id="7f7af-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-238">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-239">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-239">True</span></span>                              |
| <span data-ttu-id="7f7af-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-244">Search-Flags</span></span>           | <span data-ttu-id="7f7af-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-245">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-246">System-Flags</span></span>           | <span data-ttu-id="7f7af-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-247">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-248">Classes used in</span></span>        | [<span data-ttu-id="7f7af-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f7af-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f7af-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f7af-251">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-251">Entry</span></span> | <span data-ttu-id="7f7af-252">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-255">System-Only</span></span>            | <span data-ttu-id="7f7af-256">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-256">False</span></span>                             |
| <span data-ttu-id="7f7af-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-257">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-258">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-258">True</span></span>                              |
| <span data-ttu-id="7f7af-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-259">Is Indexed</span></span>             | <span data-ttu-id="7f7af-260">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-260">True</span></span>                              |
| <span data-ttu-id="7f7af-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-261">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-262">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-262">True</span></span>                              |
| <span data-ttu-id="7f7af-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-267">Search-Flags</span></span>           | <span data-ttu-id="7f7af-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-268">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-269">System-Flags</span></span>           | <span data-ttu-id="7f7af-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-270">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-271">Classes used in</span></span>        | [<span data-ttu-id="7f7af-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f7af-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f7af-273">Windows Server 2012</span></span>



| <span data-ttu-id="7f7af-274">Voce</span><span class="sxs-lookup"><span data-stu-id="7f7af-274">Entry</span></span> | <span data-ttu-id="7f7af-275">Valore</span><span class="sxs-lookup"><span data-stu-id="7f7af-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f7af-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f7af-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f7af-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f7af-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f7af-278">System-Only</span></span>            | <span data-ttu-id="7f7af-279">Falso</span><span class="sxs-lookup"><span data-stu-id="7f7af-279">False</span></span>                             |
| <span data-ttu-id="7f7af-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f7af-280">Is-Single-Valued</span></span>       | <span data-ttu-id="7f7af-281">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-281">True</span></span>                              |
| <span data-ttu-id="7f7af-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f7af-282">Is Indexed</span></span>             | <span data-ttu-id="7f7af-283">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-283">True</span></span>                              |
| <span data-ttu-id="7f7af-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f7af-284">In Global Catalog</span></span>      | <span data-ttu-id="7f7af-285">Vero</span><span class="sxs-lookup"><span data-stu-id="7f7af-285">True</span></span>                              |
| <span data-ttu-id="7f7af-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f7af-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f7af-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f7af-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f7af-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f7af-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f7af-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f7af-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f7af-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-290">Search-Flags</span></span>           | <span data-ttu-id="7f7af-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f7af-291">0x00000001</span></span>                        |
| <span data-ttu-id="7f7af-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f7af-292">System-Flags</span></span>           | <span data-ttu-id="7f7af-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7f7af-293">0x00000012</span></span>                        |
| <span data-ttu-id="7f7af-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f7af-294">Classes used in</span></span>        | [<span data-ttu-id="7f7af-295">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7f7af-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7f7af-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f7af-296">Remarks</span></span>

<span data-ttu-id="7f7af-297">In ADAM, questo attributo non deve essere nel formato standard Internet RFC 822; può trattarsi di un nome semplice.</span><span class="sxs-lookup"><span data-stu-id="7f7af-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

