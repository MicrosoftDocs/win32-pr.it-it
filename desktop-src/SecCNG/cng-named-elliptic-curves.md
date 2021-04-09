---
description: A partire da Windows 10, CNG fornisce il supporto per le curve ellittiche denominate seguenti (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: 'CNG: curve ellittiche denominate (Bcrypt.h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878617"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="2abc2-103">Curve ellittiche denominate CNG</span><span class="sxs-lookup"><span data-stu-id="2abc2-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="2abc2-104">A partire da Windows 10, CNG fornisce il supporto per le curve ellittiche denominate seguenti (ANSI X 9.62, X 9.63, FIPS 186-2).</span><span class="sxs-lookup"><span data-stu-id="2abc2-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="2abc2-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ecc \_ curva \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-106">Requirement</span></span> | <span data-ttu-id="2abc2-107">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="2abc2-108">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-108">Name</span></span>              | <span data-ttu-id="2abc2-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="2abc2-109">curve25519</span></span>                                                  |
| <span data-ttu-id="2abc2-110">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-110">Standard</span></span>          | [<span data-ttu-id="2abc2-111">Curva 25519</span><span class="sxs-lookup"><span data-stu-id="2abc2-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="2abc2-112">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-112">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-113">255</span><span class="sxs-lookup"><span data-stu-id="2abc2-113">255</span></span>                                                         |
| <span data-ttu-id="2abc2-114">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="2abc2-115">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-115">Object identifier</span></span> | <span data-ttu-id="2abc2-116">nessuno</span><span class="sxs-lookup"><span data-stu-id="2abc2-116">None</span></span>                                                        |



 

<span data-ttu-id="2abc2-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_ \_ BRAINPOOLP160R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-118">Requirement</span></span> | <span data-ttu-id="2abc2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-120">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-120">Name</span></span>              | <span data-ttu-id="2abc2-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-122">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-122">Standard</span></span>          | [<span data-ttu-id="2abc2-123">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-124">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-124">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-125">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-125">160</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-126">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-126">TLS capable</span></span>       | <span data-ttu-id="2abc2-127">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-127">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-128">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-128">Object identifier</span></span> | <span data-ttu-id="2abc2-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="2abc2-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-131">Requirement</span></span> | <span data-ttu-id="2abc2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-133">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-133">Name</span></span>              | <span data-ttu-id="2abc2-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-135">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-135">Standard</span></span>          | [<span data-ttu-id="2abc2-136">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-137">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-137">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-138">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-138">160</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-139">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-139">TLS capable</span></span>       | <span data-ttu-id="2abc2-140">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-140">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-141">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-141">Object identifier</span></span> | <span data-ttu-id="2abc2-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="2abc2-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_ \_ BRAINPOOLP192R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-144">Requirement</span></span> | <span data-ttu-id="2abc2-145">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-146">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-146">Name</span></span>              | <span data-ttu-id="2abc2-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-148">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-148">Standard</span></span>          | [<span data-ttu-id="2abc2-149">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-150">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-150">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-151">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-151">192</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-152">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-152">TLS capable</span></span>       | <span data-ttu-id="2abc2-153">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-153">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-154">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-154">Object identifier</span></span> | <span data-ttu-id="2abc2-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="2abc2-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_ \_ BRAINPOOLP192T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-157">Requirement</span></span> | <span data-ttu-id="2abc2-158">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-159">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-159">Name</span></span>              | <span data-ttu-id="2abc2-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-161">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-161">Standard</span></span>          | [<span data-ttu-id="2abc2-162">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-163">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-163">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-164">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-164">192</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-165">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-165">TLS capable</span></span>       | <span data-ttu-id="2abc2-166">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-166">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-167">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-167">Object identifier</span></span> | <span data-ttu-id="2abc2-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="2abc2-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_ \_ BRAINPOOLP224R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-170">Requirement</span></span> | <span data-ttu-id="2abc2-171">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-172">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-172">Name</span></span>              | <span data-ttu-id="2abc2-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-174">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-174">Standard</span></span>          | [<span data-ttu-id="2abc2-175">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-176">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-176">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-177">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-177">224</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-178">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-178">TLS capable</span></span>       | <span data-ttu-id="2abc2-179">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-179">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-180">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-180">Object identifier</span></span> | <span data-ttu-id="2abc2-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="2abc2-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_ \_ BRAINPOOLP224T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-183">Requirement</span></span> | <span data-ttu-id="2abc2-184">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-185">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-185">Name</span></span>              | <span data-ttu-id="2abc2-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-187">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-187">Standard</span></span>          | [<span data-ttu-id="2abc2-188">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-189">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-189">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-190">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-190">224</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-191">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-191">TLS capable</span></span>       | <span data-ttu-id="2abc2-192">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-192">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-193">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-193">Object identifier</span></span> | <span data-ttu-id="2abc2-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="2abc2-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_ \_ BRAINPOOLP256R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-196">Requirement</span></span> | <span data-ttu-id="2abc2-197">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-198">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-198">Name</span></span>              | <span data-ttu-id="2abc2-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-200">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-200">Standard</span></span>          | [<span data-ttu-id="2abc2-201">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-202">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-202">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-203">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-203">256</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-204">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-204">TLS capable</span></span>       | <span data-ttu-id="2abc2-205">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-206">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-206">Object identifier</span></span> | <span data-ttu-id="2abc2-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="2abc2-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_ \_ BRAINPOOLP256T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-209">Requirement</span></span> | <span data-ttu-id="2abc2-210">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-211">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-211">Name</span></span>              | <span data-ttu-id="2abc2-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-213">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-213">Standard</span></span>          | [<span data-ttu-id="2abc2-214">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-215">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-215">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-216">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-216">256</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-217">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-217">TLS capable</span></span>       | <span data-ttu-id="2abc2-218">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-218">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-219">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-219">Object identifier</span></span> | <span data-ttu-id="2abc2-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="2abc2-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_ \_ BRAINPOOLP320R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-222">Requirement</span></span> | <span data-ttu-id="2abc2-223">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-224">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-224">Name</span></span>              | <span data-ttu-id="2abc2-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-226">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-226">Standard</span></span>          | [<span data-ttu-id="2abc2-227">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-228">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-228">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-229">320</span><span class="sxs-lookup"><span data-stu-id="2abc2-229">320</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-230">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-230">TLS capable</span></span>       | <span data-ttu-id="2abc2-231">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-231">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-232">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-232">Object identifier</span></span> | <span data-ttu-id="2abc2-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="2abc2-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="2abc2-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ecc \_ curva \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-235">Requirement</span></span> | <span data-ttu-id="2abc2-236">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-237">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-237">Name</span></span>              | <span data-ttu-id="2abc2-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-239">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-239">Standard</span></span>          | [<span data-ttu-id="2abc2-240">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-241">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-241">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-242">320</span><span class="sxs-lookup"><span data-stu-id="2abc2-242">320</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-243">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-243">TLS capable</span></span>       | <span data-ttu-id="2abc2-244">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-244">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-245">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-245">Object identifier</span></span> | <span data-ttu-id="2abc2-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="2abc2-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="2abc2-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-248">Requirement</span></span> | <span data-ttu-id="2abc2-249">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-250">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-250">Name</span></span>              | <span data-ttu-id="2abc2-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-252">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-252">Standard</span></span>          | [<span data-ttu-id="2abc2-253">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-254">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-254">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-255">384</span><span class="sxs-lookup"><span data-stu-id="2abc2-255">384</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-256">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-256">TLS capable</span></span>       | <span data-ttu-id="2abc2-257">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-258">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-258">Object identifier</span></span> | <span data-ttu-id="2abc2-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="2abc2-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="2abc2-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_ \_ BRAINPOOLP384T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-261">Requirement</span></span> | <span data-ttu-id="2abc2-262">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-263">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-263">Name</span></span>              | <span data-ttu-id="2abc2-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-265">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-265">Standard</span></span>          | [<span data-ttu-id="2abc2-266">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-267">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-267">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-268">384</span><span class="sxs-lookup"><span data-stu-id="2abc2-268">384</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-269">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-269">TLS capable</span></span>       | <span data-ttu-id="2abc2-270">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-270">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-271">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-271">Object identifier</span></span> | <span data-ttu-id="2abc2-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="2abc2-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="2abc2-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_ \_ BRAINPOOLP512R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-274">Requirement</span></span> | <span data-ttu-id="2abc2-275">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-276">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-276">Name</span></span>              | <span data-ttu-id="2abc2-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-278">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-278">Standard</span></span>          | [<span data-ttu-id="2abc2-279">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-280">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-280">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-281">512</span><span class="sxs-lookup"><span data-stu-id="2abc2-281">512</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-282">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-282">TLS capable</span></span>       | <span data-ttu-id="2abc2-283">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-284">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-284">Object identifier</span></span> | <span data-ttu-id="2abc2-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="2abc2-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="2abc2-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_ \_ BRAINPOOLP512T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-287">Requirement</span></span> | <span data-ttu-id="2abc2-288">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-289">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-289">Name</span></span>              | <span data-ttu-id="2abc2-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="2abc2-291">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-291">Standard</span></span>          | [<span data-ttu-id="2abc2-292">ECC. Brainpool curve e generazione di curva standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2abc2-293">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-293">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-294">512</span><span class="sxs-lookup"><span data-stu-id="2abc2-294">512</span></span>                                                                                                               |
| <span data-ttu-id="2abc2-295">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-295">TLS capable</span></span>       | <span data-ttu-id="2abc2-296">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-296">No</span></span>                                                                                                                |
| <span data-ttu-id="2abc2-297">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-297">Object identifier</span></span> | <span data-ttu-id="2abc2-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="2abc2-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="2abc2-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-300">Requirement</span></span> | <span data-ttu-id="2abc2-301">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="2abc2-302">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-302">Name</span></span>              | <span data-ttu-id="2abc2-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="2abc2-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="2abc2-304">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-304">Standard</span></span>          | <span data-ttu-id="2abc2-305">Standard nazionale cinese per LAN wireless (GB 15629.11-2003)</span><span class="sxs-lookup"><span data-stu-id="2abc2-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="2abc2-306">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-306">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-307">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-307">192</span></span>                                                            |
| <span data-ttu-id="2abc2-308">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-308">TLS capable</span></span>       | <span data-ttu-id="2abc2-309">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-309">No</span></span>                                                             |
| <span data-ttu-id="2abc2-310">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-310">Object identifier</span></span> | <span data-ttu-id="2abc2-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="2abc2-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="2abc2-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_ \_ NISTP192 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-313">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-313">Requirement</span></span> | <span data-ttu-id="2abc2-314">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-315">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-315">Name</span></span>              | <span data-ttu-id="2abc2-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="2abc2-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="2abc2-317">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-317">Standard</span></span>          | [<span data-ttu-id="2abc2-318">Curve ellittiche consigliate per l'uso del governo federale</span><span class="sxs-lookup"><span data-stu-id="2abc2-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2abc2-319">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-319">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-320">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-321">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-321">TLS capable</span></span>       | <span data-ttu-id="2abc2-322">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-323">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-323">Object identifier</span></span> | <span data-ttu-id="2abc2-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2abc2-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="2abc2-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-326">Requirement</span></span> | <span data-ttu-id="2abc2-327">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-328">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-328">Name</span></span>              | <span data-ttu-id="2abc2-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="2abc2-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="2abc2-330">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-330">Standard</span></span>          | [<span data-ttu-id="2abc2-331">Curve ellittiche consigliate per l'uso del governo federale</span><span class="sxs-lookup"><span data-stu-id="2abc2-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2abc2-332">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-332">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-333">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-334">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-334">TLS capable</span></span>       | <span data-ttu-id="2abc2-335">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-336">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-336">Object identifier</span></span> | <span data-ttu-id="2abc2-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2abc2-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="2abc2-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_ \_ NISTP256 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-339">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-339">Requirement</span></span> | <span data-ttu-id="2abc2-340">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-341">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-341">Name</span></span>              | <span data-ttu-id="2abc2-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="2abc2-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="2abc2-343">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-343">Standard</span></span>          | [<span data-ttu-id="2abc2-344">Curve ellittiche consigliate per l'uso del governo federale</span><span class="sxs-lookup"><span data-stu-id="2abc2-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2abc2-345">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-345">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-346">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-347">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-347">TLS capable</span></span>       | <span data-ttu-id="2abc2-348">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-349">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-349">Object identifier</span></span> | <span data-ttu-id="2abc2-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2abc2-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="2abc2-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-352">Requirement</span></span> | <span data-ttu-id="2abc2-353">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-354">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-354">Name</span></span>              | <span data-ttu-id="2abc2-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="2abc2-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="2abc2-356">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-356">Standard</span></span>          | [<span data-ttu-id="2abc2-357">Curve ellittiche consigliate per l'uso del governo federale</span><span class="sxs-lookup"><span data-stu-id="2abc2-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2abc2-358">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-358">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-359">384</span><span class="sxs-lookup"><span data-stu-id="2abc2-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-360">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-360">TLS capable</span></span>       | <span data-ttu-id="2abc2-361">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-362">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-362">Object identifier</span></span> | <span data-ttu-id="2abc2-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="2abc2-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="2abc2-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_ \_ NISTP521 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-365">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-365">Requirement</span></span> | <span data-ttu-id="2abc2-366">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-367">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-367">Name</span></span>              | <span data-ttu-id="2abc2-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="2abc2-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="2abc2-369">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-369">Standard</span></span>          | [<span data-ttu-id="2abc2-370">Curve ellittiche consigliate per l'uso del governo federale</span><span class="sxs-lookup"><span data-stu-id="2abc2-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2abc2-371">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-371">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-372">521</span><span class="sxs-lookup"><span data-stu-id="2abc2-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-373">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-373">TLS capable</span></span>       | <span data-ttu-id="2abc2-374">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2abc2-375">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-375">Object identifier</span></span> | <span data-ttu-id="2abc2-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="2abc2-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="2abc2-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-378">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-378">Requirement</span></span> | <span data-ttu-id="2abc2-379">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-380">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-380">Name</span></span>              | <span data-ttu-id="2abc2-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="2abc2-382">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-382">Standard</span></span>          | [<span data-ttu-id="2abc2-383">Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="2abc2-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2abc2-384">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-384">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-385">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="2abc2-386">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-386">TLS capable</span></span>       | <span data-ttu-id="2abc2-387">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2abc2-388">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-388">Object identifier</span></span> | <span data-ttu-id="2abc2-389">nessuno</span><span class="sxs-lookup"><span data-stu-id="2abc2-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2abc2-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-391">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-391">Requirement</span></span> | <span data-ttu-id="2abc2-392">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-393">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-393">Name</span></span>              | <span data-ttu-id="2abc2-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="2abc2-395">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-395">Standard</span></span>          | [<span data-ttu-id="2abc2-396">Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="2abc2-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2abc2-397">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-397">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-398">384</span><span class="sxs-lookup"><span data-stu-id="2abc2-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="2abc2-399">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-399">TLS capable</span></span>       | <span data-ttu-id="2abc2-400">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2abc2-401">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-401">Object identifier</span></span> | <span data-ttu-id="2abc2-402">nessuno</span><span class="sxs-lookup"><span data-stu-id="2abc2-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2abc2-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_ \_ NUMSP512T1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-404">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-404">Requirement</span></span> | <span data-ttu-id="2abc2-405">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-406">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-406">Name</span></span>              | <span data-ttu-id="2abc2-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="2abc2-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="2abc2-408">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-408">Standard</span></span>          | [<span data-ttu-id="2abc2-409">Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="2abc2-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2abc2-410">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-410">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-411">512</span><span class="sxs-lookup"><span data-stu-id="2abc2-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="2abc2-412">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-412">TLS capable</span></span>       | <span data-ttu-id="2abc2-413">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2abc2-414">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-414">Object identifier</span></span> | <span data-ttu-id="2abc2-415">nessuno</span><span class="sxs-lookup"><span data-stu-id="2abc2-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2abc2-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-417">Requirement</span></span> | <span data-ttu-id="2abc2-418">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-419">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-419">Name</span></span>              | <span data-ttu-id="2abc2-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="2abc2-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="2abc2-421">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-421">Standard</span></span>          | [<span data-ttu-id="2abc2-422">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-423">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-423">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-424">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-424">160</span></span>                                                                             |
| <span data-ttu-id="2abc2-425">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-425">TLS capable</span></span>       | <span data-ttu-id="2abc2-426">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-426">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-427">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-427">Object identifier</span></span> | <span data-ttu-id="2abc2-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="2abc2-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="2abc2-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-430">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-430">Requirement</span></span> | <span data-ttu-id="2abc2-431">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-432">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-432">Name</span></span>              | <span data-ttu-id="2abc2-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-434">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-434">Standard</span></span>          | [<span data-ttu-id="2abc2-435">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-436">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-436">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-437">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-437">160</span></span>                                                                             |
| <span data-ttu-id="2abc2-438">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-438">TLS capable</span></span>       | <span data-ttu-id="2abc2-439">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-439">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-440">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-440">Object identifier</span></span> | <span data-ttu-id="2abc2-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="2abc2-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="2abc2-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-443">Requirement</span></span> | <span data-ttu-id="2abc2-444">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-445">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-445">Name</span></span>              | <span data-ttu-id="2abc2-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="2abc2-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="2abc2-447">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-447">Standard</span></span>          | [<span data-ttu-id="2abc2-448">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-449">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-449">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-450">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-450">160</span></span>                                                                             |
| <span data-ttu-id="2abc2-451">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-451">TLS capable</span></span>       | <span data-ttu-id="2abc2-452">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-452">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-453">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-453">Object identifier</span></span> | <span data-ttu-id="2abc2-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="2abc2-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="2abc2-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_ \_ SECP192K1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-456">Requirement</span></span> | <span data-ttu-id="2abc2-457">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-458">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-458">Name</span></span>              | <span data-ttu-id="2abc2-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="2abc2-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="2abc2-460">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-460">Standard</span></span>          | [<span data-ttu-id="2abc2-461">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-462">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-462">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-463">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-463">192</span></span>                                                                             |
| <span data-ttu-id="2abc2-464">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-464">TLS capable</span></span>       | <span data-ttu-id="2abc2-465">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-465">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-466">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-466">Object identifier</span></span> | <span data-ttu-id="2abc2-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="2abc2-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="2abc2-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-469">Requirement</span></span> | <span data-ttu-id="2abc2-470">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-471">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-471">Name</span></span>              | <span data-ttu-id="2abc2-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-473">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-473">Standard</span></span>          | [<span data-ttu-id="2abc2-474">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-475">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-475">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-476">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-476">192</span></span>                                                                             |
| <span data-ttu-id="2abc2-477">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-477">TLS capable</span></span>       | <span data-ttu-id="2abc2-478">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-478">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-479">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-479">Object identifier</span></span> | <span data-ttu-id="2abc2-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2abc2-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="2abc2-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_ \_ SECP224K1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-482">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-482">Requirement</span></span> | <span data-ttu-id="2abc2-483">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-484">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-484">Name</span></span>              | <span data-ttu-id="2abc2-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="2abc2-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="2abc2-486">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-486">Standard</span></span>          | [<span data-ttu-id="2abc2-487">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-488">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-488">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-489">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-489">224</span></span>                                                                             |
| <span data-ttu-id="2abc2-490">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-490">TLS capable</span></span>       | <span data-ttu-id="2abc2-491">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-491">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-492">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-492">Object identifier</span></span> | <span data-ttu-id="2abc2-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="2abc2-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="2abc2-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_ \_ SECP224R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-495">Requirement</span></span> | <span data-ttu-id="2abc2-496">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-497">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-497">Name</span></span>              | <span data-ttu-id="2abc2-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-499">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-499">Standard</span></span>          | [<span data-ttu-id="2abc2-500">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-501">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-501">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-502">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-502">224</span></span>                                                                             |
| <span data-ttu-id="2abc2-503">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-503">TLS capable</span></span>       | <span data-ttu-id="2abc2-504">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-504">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-505">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-505">Object identifier</span></span> | <span data-ttu-id="2abc2-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2abc2-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="2abc2-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_ \_ SECP256K1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-508">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-508">Requirement</span></span> | <span data-ttu-id="2abc2-509">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-510">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-510">Name</span></span>              | <span data-ttu-id="2abc2-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="2abc2-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="2abc2-512">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-512">Standard</span></span>          | [<span data-ttu-id="2abc2-513">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-514">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-514">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-515">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-515">256</span></span>                                                                             |
| <span data-ttu-id="2abc2-516">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-516">TLS capable</span></span>       | <span data-ttu-id="2abc2-517">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-517">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-518">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-518">Object identifier</span></span> | <span data-ttu-id="2abc2-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="2abc2-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="2abc2-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_ \_ SECP256R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-521">Requirement</span></span> | <span data-ttu-id="2abc2-522">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-523">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-523">Name</span></span>              | <span data-ttu-id="2abc2-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-525">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-525">Standard</span></span>          | [<span data-ttu-id="2abc2-526">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-527">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-527">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-528">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-528">256</span></span>                                                                             |
| <span data-ttu-id="2abc2-529">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-529">TLS capable</span></span>       | <span data-ttu-id="2abc2-530">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-530">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-531">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-531">Object identifier</span></span> | <span data-ttu-id="2abc2-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2abc2-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="2abc2-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-534">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-534">Requirement</span></span> | <span data-ttu-id="2abc2-535">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-536">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-536">Name</span></span>              | <span data-ttu-id="2abc2-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-538">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-538">Standard</span></span>          | [<span data-ttu-id="2abc2-539">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-540">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-540">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-541">384</span><span class="sxs-lookup"><span data-stu-id="2abc2-541">384</span></span>                                                                             |
| <span data-ttu-id="2abc2-542">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-542">TLS capable</span></span>       | <span data-ttu-id="2abc2-543">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-543">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-544">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-544">Object identifier</span></span> | <span data-ttu-id="2abc2-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="2abc2-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="2abc2-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_ \_ SECP521R1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-547">Requirement</span></span> | <span data-ttu-id="2abc2-548">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-549">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-549">Name</span></span>              | <span data-ttu-id="2abc2-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="2abc2-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="2abc2-551">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-551">Standard</span></span>          | [<span data-ttu-id="2abc2-552">Parametri di dominio curva ellittica consigliati</span><span class="sxs-lookup"><span data-stu-id="2abc2-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2abc2-553">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-553">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-554">521</span><span class="sxs-lookup"><span data-stu-id="2abc2-554">521</span></span>                                                                             |
| <span data-ttu-id="2abc2-555">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-555">TLS capable</span></span>       | <span data-ttu-id="2abc2-556">Sì</span><span class="sxs-lookup"><span data-stu-id="2abc2-556">Yes</span></span>                                                                             |
| <span data-ttu-id="2abc2-557">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-557">Object identifier</span></span> | <span data-ttu-id="2abc2-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="2abc2-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="2abc2-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_ \_ WTLS12 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-560">Requirement</span></span> | <span data-ttu-id="2abc2-561">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="2abc2-562">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-562">Name</span></span>              | <span data-ttu-id="2abc2-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="2abc2-563">wtls12</span></span>       |
| <span data-ttu-id="2abc2-564">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-564">Standard</span></span>          | <span data-ttu-id="2abc2-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-565">WTLS</span></span>         |
| <span data-ttu-id="2abc2-566">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-566">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-567">224</span><span class="sxs-lookup"><span data-stu-id="2abc2-567">224</span></span>          |
| <span data-ttu-id="2abc2-568">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-568">TLS capable</span></span>       | <span data-ttu-id="2abc2-569">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-569">No</span></span>           |
| <span data-ttu-id="2abc2-570">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-570">Object identifier</span></span> | <span data-ttu-id="2abc2-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2abc2-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="2abc2-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_ \_ WTLS7 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-573">Requirement</span></span> | <span data-ttu-id="2abc2-574">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="2abc2-575">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-575">Name</span></span>              | <span data-ttu-id="2abc2-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="2abc2-576">wtls7</span></span>        |
| <span data-ttu-id="2abc2-577">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-577">Standard</span></span>          | <span data-ttu-id="2abc2-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-578">WTLS</span></span>         |
| <span data-ttu-id="2abc2-579">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-579">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-580">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-580">160</span></span>          |
| <span data-ttu-id="2abc2-581">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-581">TLS capable</span></span>       | <span data-ttu-id="2abc2-582">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-582">No</span></span>           |
| <span data-ttu-id="2abc2-583">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-583">Object identifier</span></span> | <span data-ttu-id="2abc2-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="2abc2-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="2abc2-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-586">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-586">Requirement</span></span> | <span data-ttu-id="2abc2-587">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="2abc2-588">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-588">Name</span></span>              | <span data-ttu-id="2abc2-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="2abc2-589">wtls9</span></span>         |
| <span data-ttu-id="2abc2-590">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-590">Standard</span></span>          | <span data-ttu-id="2abc2-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-591">WTLS</span></span>          |
| <span data-ttu-id="2abc2-592">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-592">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-593">160</span><span class="sxs-lookup"><span data-stu-id="2abc2-593">160</span></span>           |
| <span data-ttu-id="2abc2-594">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-594">TLS capable</span></span>       | <span data-ttu-id="2abc2-595">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-595">No</span></span>            |
| <span data-ttu-id="2abc2-596">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-596">Object identifier</span></span> | <span data-ttu-id="2abc2-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="2abc2-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="2abc2-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_ \_ X962P192V1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-599">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-599">Requirement</span></span> | <span data-ttu-id="2abc2-600">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-601">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-601">Name</span></span>              | <span data-ttu-id="2abc2-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="2abc2-602">x962P192v1</span></span>          |
| <span data-ttu-id="2abc2-603">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-603">Standard</span></span>          | <span data-ttu-id="2abc2-604">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-605">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-605">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-606">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-606">192</span></span>                 |
| <span data-ttu-id="2abc2-607">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-607">TLS capable</span></span>       | <span data-ttu-id="2abc2-608">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-608">No</span></span>                  |
| <span data-ttu-id="2abc2-609">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-609">Object identifier</span></span> | <span data-ttu-id="2abc2-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2abc2-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="2abc2-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-612">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-612">Requirement</span></span> | <span data-ttu-id="2abc2-613">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-614">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-614">Name</span></span>              | <span data-ttu-id="2abc2-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="2abc2-615">x962P192v2</span></span>          |
| <span data-ttu-id="2abc2-616">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-616">Standard</span></span>          | <span data-ttu-id="2abc2-617">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-618">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-618">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-619">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-619">192</span></span>                 |
| <span data-ttu-id="2abc2-620">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-620">TLS capable</span></span>       | <span data-ttu-id="2abc2-621">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-621">No</span></span>                  |
| <span data-ttu-id="2abc2-622">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-622">Object identifier</span></span> | <span data-ttu-id="2abc2-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="2abc2-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="2abc2-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_ \_ X962P192V3 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-625">Requirement</span></span> | <span data-ttu-id="2abc2-626">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-627">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-627">Name</span></span>              | <span data-ttu-id="2abc2-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="2abc2-628">x962P192v3</span></span>          |
| <span data-ttu-id="2abc2-629">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-629">Standard</span></span>          | <span data-ttu-id="2abc2-630">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-631">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-631">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-632">192</span><span class="sxs-lookup"><span data-stu-id="2abc2-632">192</span></span>                 |
| <span data-ttu-id="2abc2-633">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-633">TLS capable</span></span>       | <span data-ttu-id="2abc2-634">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-634">No</span></span>                  |
| <span data-ttu-id="2abc2-635">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-635">Object identifier</span></span> | <span data-ttu-id="2abc2-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="2abc2-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="2abc2-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-638">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-638">Requirement</span></span> | <span data-ttu-id="2abc2-639">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-640">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-640">Name</span></span>              | <span data-ttu-id="2abc2-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="2abc2-641">x962P239v1</span></span>          |
| <span data-ttu-id="2abc2-642">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-642">Standard</span></span>          | <span data-ttu-id="2abc2-643">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-644">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-644">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-645">239</span><span class="sxs-lookup"><span data-stu-id="2abc2-645">239</span></span>                 |
| <span data-ttu-id="2abc2-646">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-646">TLS capable</span></span>       | <span data-ttu-id="2abc2-647">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-647">No</span></span>                  |
| <span data-ttu-id="2abc2-648">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-648">Object identifier</span></span> | <span data-ttu-id="2abc2-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="2abc2-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="2abc2-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-651">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-651">Requirement</span></span> | <span data-ttu-id="2abc2-652">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-653">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-653">Name</span></span>              | <span data-ttu-id="2abc2-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="2abc2-654">x962P239v2</span></span>          |
| <span data-ttu-id="2abc2-655">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-655">Standard</span></span>          | <span data-ttu-id="2abc2-656">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-657">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-657">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-658">239</span><span class="sxs-lookup"><span data-stu-id="2abc2-658">239</span></span>                 |
| <span data-ttu-id="2abc2-659">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-659">TLS capable</span></span>       | <span data-ttu-id="2abc2-660">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-660">No</span></span>                  |
| <span data-ttu-id="2abc2-661">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-661">Object identifier</span></span> | <span data-ttu-id="2abc2-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="2abc2-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="2abc2-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 curva ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-664">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-664">Requirement</span></span> | <span data-ttu-id="2abc2-665">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-666">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-666">Name</span></span>              | <span data-ttu-id="2abc2-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="2abc2-667">x962P239v3</span></span>          |
| <span data-ttu-id="2abc2-668">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-668">Standard</span></span>          | <span data-ttu-id="2abc2-669">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-670">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-670">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-671">239</span><span class="sxs-lookup"><span data-stu-id="2abc2-671">239</span></span>                 |
| <span data-ttu-id="2abc2-672">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-672">TLS capable</span></span>       | <span data-ttu-id="2abc2-673">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-673">No</span></span>                  |
| <span data-ttu-id="2abc2-674">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-674">Object identifier</span></span> | <span data-ttu-id="2abc2-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="2abc2-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="2abc2-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_ \_ X962P256V1 curva BCRYPT \_ ecc**</dt> </span><span class="sxs-lookup"><span data-stu-id="2abc2-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2abc2-677">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-677">Requirement</span></span> | <span data-ttu-id="2abc2-678">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2abc2-679">Nome</span><span class="sxs-lookup"><span data-stu-id="2abc2-679">Name</span></span>              | <span data-ttu-id="2abc2-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="2abc2-680">x962P256v1</span></span>          |
| <span data-ttu-id="2abc2-681">Standard</span><span class="sxs-lookup"><span data-stu-id="2abc2-681">Standard</span></span>          | <span data-ttu-id="2abc2-682">9.62 ANSI X</span><span class="sxs-lookup"><span data-stu-id="2abc2-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="2abc2-683">Dimensione chiave (bit)</span><span class="sxs-lookup"><span data-stu-id="2abc2-683">Key size (bits)</span></span>   | <span data-ttu-id="2abc2-684">256</span><span class="sxs-lookup"><span data-stu-id="2abc2-684">256</span></span>                 |
| <span data-ttu-id="2abc2-685">In grado di supportare TLS</span><span class="sxs-lookup"><span data-stu-id="2abc2-685">TLS capable</span></span>       | <span data-ttu-id="2abc2-686">No</span><span class="sxs-lookup"><span data-stu-id="2abc2-686">No</span></span>                  |
| <span data-ttu-id="2abc2-687">Identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="2abc2-687">Object identifier</span></span> | <span data-ttu-id="2abc2-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2abc2-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2abc2-689">Commenti</span><span class="sxs-lookup"><span data-stu-id="2abc2-689">Remarks</span></span>

<span data-ttu-id="2abc2-690">Per usare una curva denominata, chiamare [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) usando l'algoritmo **BCRYPT \_ ECDSA \_** o l'algoritmo **BCRYPT \_ ECDH \_** come ID algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2abc2-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="2abc2-691">Chiamare quindi [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) e impostare la proprietà **BCRYPT \_ ecc \_ curve \_ Name** su una delle curve indicate sopra o tutte le curve denominate registrate nel computer, come illustrato dal `certutil -displayEccCurve` comando.</span><span class="sxs-lookup"><span data-stu-id="2abc2-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abc2-692">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2abc2-692">Requirements</span></span>



| <span data-ttu-id="2abc2-693">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc2-693">Requirement</span></span> | <span data-ttu-id="2abc2-694">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc2-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc2-695">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2abc2-695">Minimum supported client</span></span><br/> | <span data-ttu-id="2abc2-696">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2abc2-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2abc2-697">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2abc2-697">Minimum supported server</span></span><br/> | <span data-ttu-id="2abc2-698">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2abc2-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2abc2-699">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2abc2-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="2abc2-700"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="2abc2-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abc2-701">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2abc2-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abc2-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="2abc2-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="2abc2-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="2abc2-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




