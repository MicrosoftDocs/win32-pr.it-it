---
title: Attributo Lockout-Duration
description: La quantità di tempo per cui un account è bloccato a causa del superamento del Lockout-Threshold.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Schema AD Lockout-Duration attribute
- Schema AD dell'attributo lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303009"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="7e673-105">Attributo Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="7e673-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="7e673-106">La quantità di tempo per cui un account è bloccato a causa del superamento della [**soglia di blocco**](a-lockoutthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="7e673-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="7e673-107">Questo valore viene archiviato come intero grande che rappresenta il negativo del numero di intervalli di 100 nanosecondi dal momento in cui viene superata la [**soglia di blocco**](a-lockoutthreshold.md) che deve trascorrere prima che l'account venga sbloccato.</span><span class="sxs-lookup"><span data-stu-id="7e673-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="7e673-108">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-108">Entry</span></span> | <span data-ttu-id="7e673-109">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7e673-110">CN</span><span class="sxs-lookup"><span data-stu-id="7e673-110">CN</span></span>                | <span data-ttu-id="7e673-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="7e673-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="7e673-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7e673-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7e673-113">lockoutDuration</span><span class="sxs-lookup"><span data-stu-id="7e673-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="7e673-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7e673-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="7e673-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7e673-115">Update Privilege</span></span>  | <span data-ttu-id="7e673-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="7e673-116">Domain administrator</span></span>                 |
| <span data-ttu-id="7e673-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7e673-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7e673-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-118">Attribute-Id</span></span>      | <span data-ttu-id="7e673-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="7e673-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="7e673-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e673-120">System-Id-Guid</span></span>    | <span data-ttu-id="7e673-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7e673-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7e673-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e673-122">Syntax</span></span>            | [<span data-ttu-id="7e673-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="7e673-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7e673-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7e673-124">Implementations</span></span>

-   [<span data-ttu-id="7e673-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e673-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e673-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e673-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e673-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e673-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e673-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e673-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e673-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e673-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e673-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e673-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e673-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e673-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7e673-132">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-132">Entry</span></span> | <span data-ttu-id="7e673-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-136">System-Only</span></span>            | <span data-ttu-id="7e673-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-139">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-140">Is Indexed</span></span>             | <span data-ttu-id="7e673-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-142">In Global Catalog</span></span>      | <span data-ttu-id="7e673-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-148">Search-Flags</span></span>           | <span data-ttu-id="7e673-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-150">System-Flags</span></span>           | <span data-ttu-id="7e673-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-152">Classes used in</span></span>        | [<span data-ttu-id="7e673-153">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-154">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-155">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e673-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e673-156">Windows Server 2003</span></span>



| <span data-ttu-id="7e673-157">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-157">Entry</span></span> | <span data-ttu-id="7e673-158">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-161">System-Only</span></span>            | <span data-ttu-id="7e673-162">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-164">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-165">Is Indexed</span></span>             | <span data-ttu-id="7e673-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-167">In Global Catalog</span></span>      | <span data-ttu-id="7e673-168">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-173">Search-Flags</span></span>           | <span data-ttu-id="7e673-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-175">System-Flags</span></span>           | <span data-ttu-id="7e673-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-177">Classes used in</span></span>        | [<span data-ttu-id="7e673-178">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-179">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-180">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e673-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e673-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e673-182">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-182">Entry</span></span> | <span data-ttu-id="7e673-183">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-186">System-Only</span></span>            | <span data-ttu-id="7e673-187">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-189">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-190">Is Indexed</span></span>             | <span data-ttu-id="7e673-191">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-192">In Global Catalog</span></span>      | <span data-ttu-id="7e673-193">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-198">Search-Flags</span></span>           | <span data-ttu-id="7e673-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-200">System-Flags</span></span>           | <span data-ttu-id="7e673-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-202">Classes used in</span></span>        | [<span data-ttu-id="7e673-203">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-204">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-205">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e673-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e673-206">Windows Server 2008</span></span>



| <span data-ttu-id="7e673-207">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-207">Entry</span></span> | <span data-ttu-id="7e673-208">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-211">System-Only</span></span>            | <span data-ttu-id="7e673-212">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-213">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-214">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-215">Is Indexed</span></span>             | <span data-ttu-id="7e673-216">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-217">In Global Catalog</span></span>      | <span data-ttu-id="7e673-218">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-223">Search-Flags</span></span>           | <span data-ttu-id="7e673-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-225">System-Flags</span></span>           | <span data-ttu-id="7e673-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-227">Classes used in</span></span>        | [<span data-ttu-id="7e673-228">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-229">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-230">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e673-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e673-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e673-232">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-232">Entry</span></span> | <span data-ttu-id="7e673-233">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-236">System-Only</span></span>            | <span data-ttu-id="7e673-237">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-238">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-239">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-240">Is Indexed</span></span>             | <span data-ttu-id="7e673-241">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-242">In Global Catalog</span></span>      | <span data-ttu-id="7e673-243">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-248">Search-Flags</span></span>           | <span data-ttu-id="7e673-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-250">System-Flags</span></span>           | <span data-ttu-id="7e673-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-252">Classes used in</span></span>        | [<span data-ttu-id="7e673-253">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-254">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-255">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e673-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e673-256">Windows Server 2012</span></span>



| <span data-ttu-id="7e673-257">Voce</span><span class="sxs-lookup"><span data-stu-id="7e673-257">Entry</span></span> | <span data-ttu-id="7e673-258">Valore</span><span class="sxs-lookup"><span data-stu-id="7e673-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e673-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e673-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e673-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e673-261">System-Only</span></span>            | <span data-ttu-id="7e673-262">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e673-263">Is-Single-Valued</span></span>       | <span data-ttu-id="7e673-264">Vero</span><span class="sxs-lookup"><span data-stu-id="7e673-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e673-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e673-265">Is Indexed</span></span>             | <span data-ttu-id="7e673-266">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e673-267">In Global Catalog</span></span>      | <span data-ttu-id="7e673-268">Falso</span><span class="sxs-lookup"><span data-stu-id="7e673-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="7e673-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e673-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e673-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e673-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="7e673-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e673-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e673-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="7e673-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-273">Search-Flags</span></span>           | <span data-ttu-id="7e673-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e673-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e673-275">System-Flags</span></span>           | <span data-ttu-id="7e673-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e673-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="7e673-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e673-277">Classes used in</span></span>        | [<span data-ttu-id="7e673-278">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="7e673-279">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7e673-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="7e673-280">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="7e673-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="7e673-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e673-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e673-282">**Soglia di blocco**</span><span class="sxs-lookup"><span data-stu-id="7e673-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





