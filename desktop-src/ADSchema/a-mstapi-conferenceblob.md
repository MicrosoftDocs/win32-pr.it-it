---
title: attributo ms-TAPI-Conference-BLOB
description: BLOB binario di dati che descrive le varie proprietà di una conferenza multicast TAPI. Il formato e il contenuto sono determinati dal valore dell'attributo Protocol-Id nello stesso oggetto. In genere, i dati in questo BLOB sono conformi a RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-TAPI-Conference-BLOB
- msTAPI-schema AD attributo ConferenceBlob
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303436"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="ad61f-107">attributo ms-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="ad61f-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="ad61f-108">BLOB binario di dati che descrive le varie proprietà di una conferenza multicast TAPI.</span><span class="sxs-lookup"><span data-stu-id="ad61f-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="ad61f-109">Il formato e il contenuto sono determinati dal valore dell'attributo Protocol-Id nello stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad61f-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="ad61f-110">In genere, i dati in questo BLOB sono conformi a RFC2327.</span><span class="sxs-lookup"><span data-stu-id="ad61f-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="ad61f-111">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-111">Entry</span></span> | <span data-ttu-id="ad61f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad61f-113">CN</span><span class="sxs-lookup"><span data-stu-id="ad61f-113">CN</span></span>                | <span data-ttu-id="ad61f-114">MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="ad61f-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="ad61f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ad61f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ad61f-116">msTAPI-ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="ad61f-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="ad61f-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ad61f-117">Size</span></span>              | <span data-ttu-id="ad61f-118">Può essere di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="ad61f-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="ad61f-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-119">Update Privilege</span></span>  | <span data-ttu-id="ad61f-120">Non sono richiesti privilegi speciali.</span><span class="sxs-lookup"><span data-stu-id="ad61f-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="ad61f-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-121">Update Frequency</span></span>  | <span data-ttu-id="ad61f-122">Può variare a discrezione di un proprietario di conferenza TAPI quando è necessario modificare alcuni dati relativi alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="ad61f-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="ad61f-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-123">Attribute-Id</span></span>      | <span data-ttu-id="ad61f-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="ad61f-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="ad61f-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad61f-125">System-Id-Guid</span></span>    | <span data-ttu-id="ad61f-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="ad61f-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="ad61f-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad61f-127">Syntax</span></span>            | [<span data-ttu-id="ad61f-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ad61f-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="ad61f-129">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ad61f-129">Implementations</span></span>

-   [<span data-ttu-id="ad61f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad61f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad61f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad61f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad61f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad61f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad61f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad61f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad61f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad61f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ad61f-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad61f-135">Windows Server 2003</span></span>



| <span data-ttu-id="ad61f-136">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-136">Entry</span></span> | <span data-ttu-id="ad61f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad61f-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad61f-140">System-Only</span></span>            | <span data-ttu-id="ad61f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-141">False</span></span>                                                             |
| <span data-ttu-id="ad61f-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ad61f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ad61f-143">Vero</span><span class="sxs-lookup"><span data-stu-id="ad61f-143">True</span></span>                                                              |
| <span data-ttu-id="ad61f-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ad61f-144">Is Indexed</span></span>             | <span data-ttu-id="ad61f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-145">False</span></span>                                                             |
| <span data-ttu-id="ad61f-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ad61f-146">In Global Catalog</span></span>      | <span data-ttu-id="ad61f-147">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-147">False</span></span>                                                             |
| <span data-ttu-id="ad61f-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ad61f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad61f-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ad61f-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ad61f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad61f-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad61f-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-152">Search-Flags</span></span>           | <span data-ttu-id="ad61f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad61f-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="ad61f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-154">System-Flags</span></span>           | <span data-ttu-id="ad61f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad61f-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="ad61f-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ad61f-156">Classes used in</span></span>        | [<span data-ttu-id="ad61f-157">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="ad61f-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad61f-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad61f-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad61f-159">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-159">Entry</span></span> | <span data-ttu-id="ad61f-160">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad61f-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad61f-163">System-Only</span></span>            | <span data-ttu-id="ad61f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-164">False</span></span>                                                             |
| <span data-ttu-id="ad61f-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ad61f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ad61f-166">Vero</span><span class="sxs-lookup"><span data-stu-id="ad61f-166">True</span></span>                                                              |
| <span data-ttu-id="ad61f-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ad61f-167">Is Indexed</span></span>             | <span data-ttu-id="ad61f-168">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-168">False</span></span>                                                             |
| <span data-ttu-id="ad61f-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ad61f-169">In Global Catalog</span></span>      | <span data-ttu-id="ad61f-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-170">False</span></span>                                                             |
| <span data-ttu-id="ad61f-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ad61f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad61f-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ad61f-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ad61f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad61f-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad61f-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-175">Search-Flags</span></span>           | <span data-ttu-id="ad61f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad61f-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="ad61f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-177">System-Flags</span></span>           | <span data-ttu-id="ad61f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad61f-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="ad61f-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ad61f-179">Classes used in</span></span>        | [<span data-ttu-id="ad61f-180">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="ad61f-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad61f-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad61f-181">Windows Server 2008</span></span>



| <span data-ttu-id="ad61f-182">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-182">Entry</span></span> | <span data-ttu-id="ad61f-183">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad61f-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad61f-186">System-Only</span></span>            | <span data-ttu-id="ad61f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-187">False</span></span>                                                             |
| <span data-ttu-id="ad61f-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ad61f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ad61f-189">Vero</span><span class="sxs-lookup"><span data-stu-id="ad61f-189">True</span></span>                                                              |
| <span data-ttu-id="ad61f-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ad61f-190">Is Indexed</span></span>             | <span data-ttu-id="ad61f-191">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-191">False</span></span>                                                             |
| <span data-ttu-id="ad61f-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ad61f-192">In Global Catalog</span></span>      | <span data-ttu-id="ad61f-193">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-193">False</span></span>                                                             |
| <span data-ttu-id="ad61f-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ad61f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad61f-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ad61f-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ad61f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad61f-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad61f-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-198">Search-Flags</span></span>           | <span data-ttu-id="ad61f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad61f-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="ad61f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-200">System-Flags</span></span>           | <span data-ttu-id="ad61f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad61f-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="ad61f-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ad61f-202">Classes used in</span></span>        | [<span data-ttu-id="ad61f-203">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="ad61f-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad61f-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad61f-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad61f-205">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-205">Entry</span></span> | <span data-ttu-id="ad61f-206">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad61f-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad61f-209">System-Only</span></span>            | <span data-ttu-id="ad61f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-210">False</span></span>                                                             |
| <span data-ttu-id="ad61f-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ad61f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ad61f-212">Vero</span><span class="sxs-lookup"><span data-stu-id="ad61f-212">True</span></span>                                                              |
| <span data-ttu-id="ad61f-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ad61f-213">Is Indexed</span></span>             | <span data-ttu-id="ad61f-214">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-214">False</span></span>                                                             |
| <span data-ttu-id="ad61f-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ad61f-215">In Global Catalog</span></span>      | <span data-ttu-id="ad61f-216">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-216">False</span></span>                                                             |
| <span data-ttu-id="ad61f-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ad61f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad61f-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ad61f-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ad61f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad61f-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad61f-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-221">Search-Flags</span></span>           | <span data-ttu-id="ad61f-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad61f-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="ad61f-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-223">System-Flags</span></span>           | <span data-ttu-id="ad61f-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad61f-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="ad61f-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ad61f-225">Classes used in</span></span>        | [<span data-ttu-id="ad61f-226">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="ad61f-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad61f-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad61f-227">Windows Server 2012</span></span>



| <span data-ttu-id="ad61f-228">Voce</span><span class="sxs-lookup"><span data-stu-id="ad61f-228">Entry</span></span> | <span data-ttu-id="ad61f-229">Valore</span><span class="sxs-lookup"><span data-stu-id="ad61f-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad61f-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ad61f-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad61f-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ad61f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad61f-232">System-Only</span></span>            | <span data-ttu-id="ad61f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-233">False</span></span>                                                             |
| <span data-ttu-id="ad61f-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ad61f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ad61f-235">Vero</span><span class="sxs-lookup"><span data-stu-id="ad61f-235">True</span></span>                                                              |
| <span data-ttu-id="ad61f-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ad61f-236">Is Indexed</span></span>             | <span data-ttu-id="ad61f-237">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-237">False</span></span>                                                             |
| <span data-ttu-id="ad61f-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ad61f-238">In Global Catalog</span></span>      | <span data-ttu-id="ad61f-239">Falso</span><span class="sxs-lookup"><span data-stu-id="ad61f-239">False</span></span>                                                             |
| <span data-ttu-id="ad61f-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ad61f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad61f-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ad61f-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ad61f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad61f-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad61f-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ad61f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-244">Search-Flags</span></span>           | <span data-ttu-id="ad61f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad61f-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="ad61f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad61f-246">System-Flags</span></span>           | <span data-ttu-id="ad61f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad61f-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="ad61f-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ad61f-248">Classes used in</span></span>        | [<span data-ttu-id="ad61f-249">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="ad61f-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





