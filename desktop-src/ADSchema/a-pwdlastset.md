---
title: Pwd-ultimo attributo set
description: Data e ora dell'Ultima modifica della password per l'account.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-ultimo-imposta schema AD dell'attributo
- Schema AD dell'attributo pwdLastSet
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303379"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="f11a5-105">Pwd-ultimo attributo set</span><span class="sxs-lookup"><span data-stu-id="f11a5-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="f11a5-106">Data e ora dell'Ultima modifica della password per l'account.</span><span class="sxs-lookup"><span data-stu-id="f11a5-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="f11a5-107">Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="f11a5-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="f11a5-108">Se questo valore è impostato su 0 e l'attributo [**User-Account-Control**](a-useraccountcontrol.md) non contiene il flag **di \_ \_ \_ passwd non scaduto** , l'utente deve impostare la password al successivo accesso.</span><span class="sxs-lookup"><span data-stu-id="f11a5-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="f11a5-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-109">Entry</span></span> | <span data-ttu-id="f11a5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f11a5-111">CN</span><span class="sxs-lookup"><span data-stu-id="f11a5-111">CN</span></span>                | <span data-ttu-id="f11a5-112">Pwd-ultimo set</span><span class="sxs-lookup"><span data-stu-id="f11a5-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="f11a5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f11a5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f11a5-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="f11a5-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="f11a5-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f11a5-115">Size</span></span>              | <span data-ttu-id="f11a5-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="f11a5-116">8 bytes</span></span>                              |
| <span data-ttu-id="f11a5-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-117">Update Privilege</span></span>  | <span data-ttu-id="f11a5-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f11a5-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="f11a5-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-119">Update Frequency</span></span>  | <span data-ttu-id="f11a5-120">Ogni volta che la password viene modificata.</span><span class="sxs-lookup"><span data-stu-id="f11a5-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="f11a5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-121">Attribute-Id</span></span>      | <span data-ttu-id="f11a5-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="f11a5-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="f11a5-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f11a5-123">System-Id-Guid</span></span>    | <span data-ttu-id="f11a5-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f11a5-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f11a5-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f11a5-125">Syntax</span></span>            | [<span data-ttu-id="f11a5-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="f11a5-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f11a5-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f11a5-127">Implementations</span></span>

-   [<span data-ttu-id="f11a5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f11a5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f11a5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f11a5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f11a5-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f11a5-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f11a5-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f11a5-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f11a5-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f11a5-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f11a5-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f11a5-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f11a5-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f11a5-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f11a5-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f11a5-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f11a5-136">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-136">Entry</span></span> | <span data-ttu-id="f11a5-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-140">System-Only</span></span>            | <span data-ttu-id="f11a5-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-141">False</span></span>                             |
| <span data-ttu-id="f11a5-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-143">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-143">True</span></span>                              |
| <span data-ttu-id="f11a5-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-144">Is Indexed</span></span>             | <span data-ttu-id="f11a5-145">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-145">False</span></span>                             |
| <span data-ttu-id="f11a5-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-146">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-147">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-147">False</span></span>                             |
| <span data-ttu-id="f11a5-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-152">Search-Flags</span></span>           | <span data-ttu-id="f11a5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-153">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-154">System-Flags</span></span>           | <span data-ttu-id="f11a5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-155">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-156">Classes used in</span></span>        | [<span data-ttu-id="f11a5-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f11a5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f11a5-158">Windows Server 2003</span></span>



| <span data-ttu-id="f11a5-159">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-159">Entry</span></span> | <span data-ttu-id="f11a5-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-163">System-Only</span></span>            | <span data-ttu-id="f11a5-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-164">False</span></span>                             |
| <span data-ttu-id="f11a5-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-166">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-166">True</span></span>                              |
| <span data-ttu-id="f11a5-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-167">Is Indexed</span></span>             | <span data-ttu-id="f11a5-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-168">False</span></span>                             |
| <span data-ttu-id="f11a5-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-169">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-170">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-170">False</span></span>                             |
| <span data-ttu-id="f11a5-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-175">Search-Flags</span></span>           | <span data-ttu-id="f11a5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-176">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-177">System-Flags</span></span>           | <span data-ttu-id="f11a5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-178">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-179">Classes used in</span></span>        | [<span data-ttu-id="f11a5-180">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f11a5-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="f11a5-181">ADAM</span></span>



| <span data-ttu-id="f11a5-182">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-182">Entry</span></span> | <span data-ttu-id="f11a5-183">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f11a5-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f11a5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f11a5-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-186">System-Only</span></span>            | <span data-ttu-id="f11a5-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-187">False</span></span>                                                             |
| <span data-ttu-id="f11a5-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-189">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-189">True</span></span>                                                              |
| <span data-ttu-id="f11a5-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-190">Is Indexed</span></span>             | <span data-ttu-id="f11a5-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-191">False</span></span>                                                             |
| <span data-ttu-id="f11a5-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-192">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-193">False</span></span>                                                             |
| <span data-ttu-id="f11a5-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f11a5-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f11a5-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f11a5-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-198">Search-Flags</span></span>           | <span data-ttu-id="f11a5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="f11a5-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-200">System-Flags</span></span>           | <span data-ttu-id="f11a5-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="f11a5-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-202">Classes used in</span></span>        | [<span data-ttu-id="f11a5-203">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="f11a5-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f11a5-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f11a5-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f11a5-205">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-205">Entry</span></span> | <span data-ttu-id="f11a5-206">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-209">System-Only</span></span>            | <span data-ttu-id="f11a5-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-210">False</span></span>                             |
| <span data-ttu-id="f11a5-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-212">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-212">True</span></span>                              |
| <span data-ttu-id="f11a5-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-213">Is Indexed</span></span>             | <span data-ttu-id="f11a5-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-214">False</span></span>                             |
| <span data-ttu-id="f11a5-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-215">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-216">False</span></span>                             |
| <span data-ttu-id="f11a5-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-221">Search-Flags</span></span>           | <span data-ttu-id="f11a5-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-222">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-223">System-Flags</span></span>           | <span data-ttu-id="f11a5-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-224">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-225">Classes used in</span></span>        | [<span data-ttu-id="f11a5-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f11a5-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f11a5-227">Windows Server 2008</span></span>



| <span data-ttu-id="f11a5-228">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-228">Entry</span></span> | <span data-ttu-id="f11a5-229">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-232">System-Only</span></span>            | <span data-ttu-id="f11a5-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-233">False</span></span>                             |
| <span data-ttu-id="f11a5-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-235">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-235">True</span></span>                              |
| <span data-ttu-id="f11a5-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-236">Is Indexed</span></span>             | <span data-ttu-id="f11a5-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-237">False</span></span>                             |
| <span data-ttu-id="f11a5-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-238">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-239">False</span></span>                             |
| <span data-ttu-id="f11a5-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-244">Search-Flags</span></span>           | <span data-ttu-id="f11a5-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-245">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-246">System-Flags</span></span>           | <span data-ttu-id="f11a5-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-247">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-248">Classes used in</span></span>        | [<span data-ttu-id="f11a5-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f11a5-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f11a5-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f11a5-251">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-251">Entry</span></span> | <span data-ttu-id="f11a5-252">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-255">System-Only</span></span>            | <span data-ttu-id="f11a5-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-256">False</span></span>                             |
| <span data-ttu-id="f11a5-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-258">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-258">True</span></span>                              |
| <span data-ttu-id="f11a5-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-259">Is Indexed</span></span>             | <span data-ttu-id="f11a5-260">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-260">False</span></span>                             |
| <span data-ttu-id="f11a5-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-261">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-262">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-262">False</span></span>                             |
| <span data-ttu-id="f11a5-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-267">Search-Flags</span></span>           | <span data-ttu-id="f11a5-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-268">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-269">System-Flags</span></span>           | <span data-ttu-id="f11a5-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-270">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-271">Classes used in</span></span>        | [<span data-ttu-id="f11a5-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f11a5-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f11a5-273">Windows Server 2012</span></span>



| <span data-ttu-id="f11a5-274">Voce</span><span class="sxs-lookup"><span data-stu-id="f11a5-274">Entry</span></span> | <span data-ttu-id="f11a5-275">Valore</span><span class="sxs-lookup"><span data-stu-id="f11a5-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f11a5-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f11a5-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f11a5-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f11a5-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="f11a5-278">System-Only</span></span>            | <span data-ttu-id="f11a5-279">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-279">False</span></span>                             |
| <span data-ttu-id="f11a5-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f11a5-280">Is-Single-Valued</span></span>       | <span data-ttu-id="f11a5-281">Vero</span><span class="sxs-lookup"><span data-stu-id="f11a5-281">True</span></span>                              |
| <span data-ttu-id="f11a5-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f11a5-282">Is Indexed</span></span>             | <span data-ttu-id="f11a5-283">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-283">False</span></span>                             |
| <span data-ttu-id="f11a5-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f11a5-284">In Global Catalog</span></span>      | <span data-ttu-id="f11a5-285">Falso</span><span class="sxs-lookup"><span data-stu-id="f11a5-285">False</span></span>                             |
| <span data-ttu-id="f11a5-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f11a5-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="f11a5-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f11a5-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f11a5-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f11a5-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f11a5-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f11a5-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f11a5-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-290">Search-Flags</span></span>           | <span data-ttu-id="f11a5-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f11a5-291">0x00000000</span></span>                        |
| <span data-ttu-id="f11a5-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f11a5-292">System-Flags</span></span>           | <span data-ttu-id="f11a5-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f11a5-293">0x00000010</span></span>                        |
| <span data-ttu-id="f11a5-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f11a5-294">Classes used in</span></span>        | [<span data-ttu-id="f11a5-295">**Utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f11a5-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="f11a5-296">Remarks</span></span>

<span data-ttu-id="f11a5-297">La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="f11a5-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="f11a5-298">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f11a5-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11a5-299">**Controllo account utente**</span><span class="sxs-lookup"><span data-stu-id="f11a5-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

