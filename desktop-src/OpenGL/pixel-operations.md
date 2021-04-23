---
title: Operazioni sui pixel
description: Operazioni sui pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- OpenGL per le operazioni sui pixel
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908879"
---
# <a name="pixel-operations"></a><span data-ttu-id="12675-104">Operazioni sui pixel</span><span class="sxs-lookup"><span data-stu-id="12675-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="12675-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>TEST \_ DI SCISSOR \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="12675-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-106">Property</span></span> | <span data-ttu-id="12675-107">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-108">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-108">Description:</span></span>     | <span data-ttu-id="12675-109">Scissoring abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="12675-110">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-110">Attribute group:</span></span> | <span data-ttu-id="12675-111">scissor/enable</span><span class="sxs-lookup"><span data-stu-id="12675-111">scissor/enable</span></span>                     |
| <span data-ttu-id="12675-112">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-112">Initial value:</span></span>   | <span data-ttu-id="12675-113">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-114">Get command:</span></span>     | [<span data-ttu-id="12675-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ SCISSOR \_ BOX</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="12675-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-117">Property</span></span> | <span data-ttu-id="12675-118">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-119">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-119">Description:</span></span>     | <span data-ttu-id="12675-120">Casella di forbice</span><span class="sxs-lookup"><span data-stu-id="12675-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="12675-121">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-121">Attribute group:</span></span> | <span data-ttu-id="12675-122">Forbice</span><span class="sxs-lookup"><span data-stu-id="12675-122">scissor</span></span>                                                                          |
| <span data-ttu-id="12675-123">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="12675-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-124">Get command:</span></span>     | [<span data-ttu-id="12675-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>TEST DI STENCIL GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="12675-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-127">Property</span></span> | <span data-ttu-id="12675-128">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-129">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-129">Description:</span></span>     | <span data-ttu-id="12675-130">Stencil abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="12675-131">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-131">Attribute group:</span></span> | <span data-ttu-id="12675-132">stencil-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="12675-133">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-133">Initial value:</span></span>   | <span data-ttu-id="12675-134">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-135">Get command:</span></span>     | [<span data-ttu-id="12675-136">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL \_ STENCIL \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="12675-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-138">Property</span></span> | <span data-ttu-id="12675-139">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-140">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-140">Description:</span></span>     | <span data-ttu-id="12675-141">Funzione Stencil</span><span class="sxs-lookup"><span data-stu-id="12675-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="12675-142">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-142">Attribute group:</span></span> | <span data-ttu-id="12675-143">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-144">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-144">Initial value:</span></span>   | <span data-ttu-id="12675-145">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="12675-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="12675-146">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-146">Get command:</span></span>     | [<span data-ttu-id="12675-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>MASCHERA VALORE STENCIL GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="12675-149">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-149">Property</span></span> | <span data-ttu-id="12675-150">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-151">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-151">Description:</span></span>     | <span data-ttu-id="12675-152">Maschera stencil</span><span class="sxs-lookup"><span data-stu-id="12675-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="12675-153">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-153">Attribute group:</span></span> | <span data-ttu-id="12675-154">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-155">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-155">Initial value:</span></span>   | <span data-ttu-id="12675-156">1 di</span><span class="sxs-lookup"><span data-stu-id="12675-156">1's</span></span>                                                                              |
| <span data-ttu-id="12675-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-157">Get command:</span></span>     | [<span data-ttu-id="12675-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ STENCIL \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="12675-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-160">Property</span></span> | <span data-ttu-id="12675-161">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-162">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-162">Description:</span></span>     | <span data-ttu-id="12675-163">Valore di riferimento dello stencil</span><span class="sxs-lookup"><span data-stu-id="12675-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="12675-164">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-164">Attribute group:</span></span> | <span data-ttu-id="12675-165">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-166">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-166">Initial value:</span></span>   | <span data-ttu-id="12675-167">0</span><span class="sxs-lookup"><span data-stu-id="12675-167">0</span></span>                                                                                |
| <span data-ttu-id="12675-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-168">Get command:</span></span>     | [<span data-ttu-id="12675-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>ESITO \_ NEGATIVO DI GL STENCIL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="12675-171">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-171">Property</span></span> | <span data-ttu-id="12675-172">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-173">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-173">Description:</span></span>     | <span data-ttu-id="12675-174">Azione di errore dello stencil</span><span class="sxs-lookup"><span data-stu-id="12675-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="12675-175">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-175">Attribute group:</span></span> | <span data-ttu-id="12675-176">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-177">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-177">Initial value:</span></span>   | <span data-ttu-id="12675-178">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="12675-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="12675-179">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-179">Get command:</span></span>     | [<span data-ttu-id="12675-180">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL \_ STENCIL \_ PASS \_ DEPTH \_ FAIL</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="12675-182">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-182">Property</span></span> | <span data-ttu-id="12675-183">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-184">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-184">Description:</span></span>     | <span data-ttu-id="12675-185">Azione di errore del buffer di profondità dello stencil</span><span class="sxs-lookup"><span data-stu-id="12675-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="12675-186">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-186">Attribute group:</span></span> | <span data-ttu-id="12675-187">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-188">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-188">Initial value:</span></span>   | <span data-ttu-id="12675-189">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="12675-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="12675-190">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-190">Get command:</span></span>     | [<span data-ttu-id="12675-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL \_ STENCIL PASS DEPTH PASS \_ \_ (PASSAGGIO DI PROFONDITÀ PASSAGGIO STENCIL \_ GL)</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="12675-193">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-193">Property</span></span> | <span data-ttu-id="12675-194">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-195">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-195">Description:</span></span>     | <span data-ttu-id="12675-196">Azione di passaggio del buffer di profondità stencil</span><span class="sxs-lookup"><span data-stu-id="12675-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="12675-197">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-197">Attribute group:</span></span> | <span data-ttu-id="12675-198">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="12675-199">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-199">Initial value:</span></span>   | <span data-ttu-id="12675-200">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="12675-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="12675-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-201">Get command:</span></span>     | [<span data-ttu-id="12675-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ TEST</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="12675-204">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-204">Property</span></span> | <span data-ttu-id="12675-205">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-206">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-206">Description:</span></span>     | <span data-ttu-id="12675-207">Test alfa abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="12675-208">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-208">Attribute group:</span></span> | <span data-ttu-id="12675-209">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="12675-210">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-210">Initial value:</span></span>   | <span data-ttu-id="12675-211">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-212">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-212">Get command:</span></span>     | [<span data-ttu-id="12675-213">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>FUNC \_ DI TEST GL ALPHA \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="12675-215">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-215">Property</span></span> | <span data-ttu-id="12675-216">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-217">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-217">Description:</span></span>     | <span data-ttu-id="12675-218">Funzione di test alfa</span><span class="sxs-lookup"><span data-stu-id="12675-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="12675-219">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-219">Attribute group:</span></span> | <span data-ttu-id="12675-220">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="12675-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-221">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-221">Initial value:</span></span>   | <span data-ttu-id="12675-222">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="12675-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="12675-223">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-223">Get command:</span></span>     | [<span data-ttu-id="12675-224">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ TEST \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="12675-226">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-226">Property</span></span> | <span data-ttu-id="12675-227">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-228">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-228">Description:</span></span>     | <span data-ttu-id="12675-229">Valore di riferimento del test alfa</span><span class="sxs-lookup"><span data-stu-id="12675-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="12675-230">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-230">Attribute group:</span></span> | <span data-ttu-id="12675-231">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="12675-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-232">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-232">Initial value:</span></span>   | <span data-ttu-id="12675-233">0</span><span class="sxs-lookup"><span data-stu-id="12675-233">0</span></span>                                                                                |
| <span data-ttu-id="12675-234">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-234">Get command:</span></span>     | [<span data-ttu-id="12675-235">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>TEST DI \_ PROFONDITÀ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="12675-237">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-237">Property</span></span> | <span data-ttu-id="12675-238">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-239">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-239">Description:</span></span>     | <span data-ttu-id="12675-240">Buffer di profondità abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="12675-241">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-241">Attribute group:</span></span> | <span data-ttu-id="12675-242">depth-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="12675-243">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-243">Initial value:</span></span>   | <span data-ttu-id="12675-244">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-245">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-245">Get command:</span></span>     | [<span data-ttu-id="12675-246">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ DEPTH \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="12675-248">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-248">Property</span></span> | <span data-ttu-id="12675-249">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-250">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-250">Description:</span></span>     | <span data-ttu-id="12675-251">Funzione di test del buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="12675-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="12675-252">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-252">Attribute group:</span></span> | <span data-ttu-id="12675-253">depth-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-254">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-254">Initial value:</span></span>   | <span data-ttu-id="12675-255">GL \_ LESS</span><span class="sxs-lookup"><span data-stu-id="12675-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="12675-256">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-256">Get command:</span></span>     | [<span data-ttu-id="12675-257">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="12675-259">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-259">Property</span></span> | <span data-ttu-id="12675-260">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-261">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-261">Description:</span></span>     | <span data-ttu-id="12675-262">Blending abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-262">Blending enabled</span></span>                   |
| <span data-ttu-id="12675-263">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-263">Attribute group:</span></span> | <span data-ttu-id="12675-264">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="12675-265">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-265">Initial value:</span></span>   | <span data-ttu-id="12675-266">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-267">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-267">Get command:</span></span>     | [<span data-ttu-id="12675-268">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="12675-270">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-270">Property</span></span> | <span data-ttu-id="12675-271">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-272">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-272">Description:</span></span>     | <span data-ttu-id="12675-273">Funzione di origine di fusione</span><span class="sxs-lookup"><span data-stu-id="12675-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="12675-274">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-274">Attribute group:</span></span> | <span data-ttu-id="12675-275">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="12675-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-276">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-276">Initial value:</span></span>   | <span data-ttu-id="12675-277">GL \_ ONE</span><span class="sxs-lookup"><span data-stu-id="12675-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="12675-278">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-278">Get command:</span></span>     | [<span data-ttu-id="12675-279">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>ORA \_ LEGALE GL BLEND \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="12675-281">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-281">Property</span></span> | <span data-ttu-id="12675-282">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-283">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-283">Description:</span></span>     | <span data-ttu-id="12675-284">Funzione di destinazione di fusione</span><span class="sxs-lookup"><span data-stu-id="12675-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="12675-285">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-285">Attribute group:</span></span> | <span data-ttu-id="12675-286">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="12675-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-287">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-287">Initial value:</span></span>   | <span data-ttu-id="12675-288">GL \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="12675-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="12675-289">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-289">Get command:</span></span>     | [<span data-ttu-id="12675-290">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="12675-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_DITHERING GL</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="12675-292">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-292">Property</span></span> | <span data-ttu-id="12675-293">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-294">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-294">Description:</span></span>     | <span data-ttu-id="12675-295">Dithering abilitato</span><span class="sxs-lookup"><span data-stu-id="12675-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="12675-296">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-296">Attribute group:</span></span> | <span data-ttu-id="12675-297">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="12675-298">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-298">Initial value:</span></span>   | <span data-ttu-id="12675-299">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="12675-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="12675-300">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-300">Get command:</span></span>     | [<span data-ttu-id="12675-301">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ LOGIC \_ OP</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="12675-303">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-303">Property</span></span> | <span data-ttu-id="12675-304">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="12675-305">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-305">Description:</span></span>     | <span data-ttu-id="12675-306">Operazione logica abilitata</span><span class="sxs-lookup"><span data-stu-id="12675-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="12675-307">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-307">Attribute group:</span></span> | <span data-ttu-id="12675-308">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="12675-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="12675-309">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-309">Initial value:</span></span>   | <span data-ttu-id="12675-310">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12675-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="12675-311">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-311">Get command:</span></span>     | [<span data-ttu-id="12675-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="12675-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="12675-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>MODALITÀ \_ DI LAVORO \_ LOGICA GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="12675-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="12675-314">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12675-314">Property</span></span> | <span data-ttu-id="12675-315">Valore</span><span class="sxs-lookup"><span data-stu-id="12675-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12675-316">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="12675-316">Description:</span></span>     | <span data-ttu-id="12675-317">Funzione dell'operazione logica</span><span class="sxs-lookup"><span data-stu-id="12675-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="12675-318">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="12675-318">Attribute group:</span></span> | <span data-ttu-id="12675-319">color-buffer</span><span class="sxs-lookup"><span data-stu-id="12675-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="12675-320">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="12675-320">Initial value:</span></span>   | <span data-ttu-id="12675-321">COPIA \_ GL</span><span class="sxs-lookup"><span data-stu-id="12675-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="12675-322">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="12675-322">Get command:</span></span>     | [<span data-ttu-id="12675-323">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="12675-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




