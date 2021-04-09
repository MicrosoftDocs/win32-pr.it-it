---
title: Operazioni pixel
description: Operazioni pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operazioni pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857274"
---
# <a name="pixel-operations"></a><span data-ttu-id="303e7-104">Operazioni pixel</span><span class="sxs-lookup"><span data-stu-id="303e7-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="303e7-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_test della forbice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-106">Description:</span></span>     | <span data-ttu-id="303e7-107">Scissoring abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="303e7-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-108">Attribute group:</span></span> | <span data-ttu-id="303e7-109">Scissor/Enable</span><span class="sxs-lookup"><span data-stu-id="303e7-109">scissor/enable</span></span>                     |
| <span data-ttu-id="303e7-110">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-110">Initial value:</span></span>   | <span data-ttu-id="303e7-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-112">Get command:</span></span>     | [<span data-ttu-id="303e7-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_casella della forbice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-115">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-115">Description:</span></span>     | <span data-ttu-id="303e7-116">Casella Scissor</span><span class="sxs-lookup"><span data-stu-id="303e7-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="303e7-117">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-117">Attribute group:</span></span> | <span data-ttu-id="303e7-118">ritaglio</span><span class="sxs-lookup"><span data-stu-id="303e7-118">scissor</span></span>                                                                          |
| <span data-ttu-id="303e7-119">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="303e7-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-120">Get command:</span></span>     | [<span data-ttu-id="303e7-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_test stencil \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-123">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-123">Description:</span></span>     | <span data-ttu-id="303e7-124">Stencil abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="303e7-125">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-125">Attribute group:</span></span> | <span data-ttu-id="303e7-126">stencil-buffer/Abilita</span><span class="sxs-lookup"><span data-stu-id="303e7-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="303e7-127">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-127">Initial value:</span></span>   | <span data-ttu-id="303e7-128">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-129">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-129">Get command:</span></span>     | [<span data-ttu-id="303e7-130">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>funzione \_ stencil \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-132">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-132">Description:</span></span>     | <span data-ttu-id="303e7-133">Funzione stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="303e7-134">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-134">Attribute group:</span></span> | <span data-ttu-id="303e7-135">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-136">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-136">Initial value:</span></span>   | <span data-ttu-id="303e7-137">GL \_ Always</span><span class="sxs-lookup"><span data-stu-id="303e7-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="303e7-138">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-138">Get command:</span></span>     | [<span data-ttu-id="303e7-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_maschera del \_ valore dello stencil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-141">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-141">Description:</span></span>     | <span data-ttu-id="303e7-142">Maschera stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="303e7-143">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-143">Attribute group:</span></span> | <span data-ttu-id="303e7-144">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-145">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-145">Initial value:</span></span>   | <span data-ttu-id="303e7-146">1</span><span class="sxs-lookup"><span data-stu-id="303e7-146">1's</span></span>                                                                              |
| <span data-ttu-id="303e7-147">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-147">Get command:</span></span>     | [<span data-ttu-id="303e7-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_riferimento allo stencil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-150">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-150">Description:</span></span>     | <span data-ttu-id="303e7-151">Valore riferimento stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="303e7-152">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-152">Attribute group:</span></span> | <span data-ttu-id="303e7-153">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-154">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-154">Initial value:</span></span>   | <span data-ttu-id="303e7-155">0</span><span class="sxs-lookup"><span data-stu-id="303e7-155">0</span></span>                                                                                |
| <span data-ttu-id="303e7-156">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-156">Get command:</span></span>     | [<span data-ttu-id="303e7-157">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_stencil GL \_ non riuscito</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-159">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-159">Description:</span></span>     | <span data-ttu-id="303e7-160">Azione di errore stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="303e7-161">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-161">Attribute group:</span></span> | <span data-ttu-id="303e7-162">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-163">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-163">Initial value:</span></span>   | <span data-ttu-id="303e7-164">\_conservazione GL</span><span class="sxs-lookup"><span data-stu-id="303e7-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="303e7-165">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-165">Get command:</span></span>     | [<span data-ttu-id="303e7-166">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_errore di \_ profondità del passaggio dello stencil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-168">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-168">Description:</span></span>     | <span data-ttu-id="303e7-169">Azione errore buffer profondità stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="303e7-170">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-170">Attribute group:</span></span> | <span data-ttu-id="303e7-171">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-172">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-172">Initial value:</span></span>   | <span data-ttu-id="303e7-173">\_conservazione GL</span><span class="sxs-lookup"><span data-stu-id="303e7-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="303e7-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-174">Get command:</span></span>     | [<span data-ttu-id="303e7-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_passaggio di \_ profondità del passaggio dello stencil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-177">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-177">Description:</span></span>     | <span data-ttu-id="303e7-178">Azione passaggio buffer profondità stencil</span><span class="sxs-lookup"><span data-stu-id="303e7-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="303e7-179">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-179">Attribute group:</span></span> | <span data-ttu-id="303e7-180">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="303e7-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="303e7-181">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-181">Initial value:</span></span>   | <span data-ttu-id="303e7-182">\_conservazione GL</span><span class="sxs-lookup"><span data-stu-id="303e7-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="303e7-183">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-183">Get command:</span></span>     | [<span data-ttu-id="303e7-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_test GL Alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-186">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-186">Description:</span></span>     | <span data-ttu-id="303e7-187">Test alfa abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="303e7-188">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-188">Attribute group:</span></span> | <span data-ttu-id="303e7-189">colore-buffer/Abilita</span><span class="sxs-lookup"><span data-stu-id="303e7-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="303e7-190">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-190">Initial value:</span></span>   | <span data-ttu-id="303e7-191">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-192">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-192">Get command:</span></span>     | [<span data-ttu-id="303e7-193">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>funzione \_ di \_ test GL Alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-195">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-195">Description:</span></span>     | <span data-ttu-id="303e7-196">Funzione di test Alpha</span><span class="sxs-lookup"><span data-stu-id="303e7-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="303e7-197">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-197">Attribute group:</span></span> | <span data-ttu-id="303e7-198">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="303e7-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-199">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-199">Initial value:</span></span>   | <span data-ttu-id="303e7-200">GL \_ Always</span><span class="sxs-lookup"><span data-stu-id="303e7-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="303e7-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-201">Get command:</span></span>     | [<span data-ttu-id="303e7-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_ref del \_ test GL Alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-204">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-204">Description:</span></span>     | <span data-ttu-id="303e7-205">Valore di riferimento del test alfa</span><span class="sxs-lookup"><span data-stu-id="303e7-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="303e7-206">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-206">Attribute group:</span></span> | <span data-ttu-id="303e7-207">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="303e7-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-208">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-208">Initial value:</span></span>   | <span data-ttu-id="303e7-209">0</span><span class="sxs-lookup"><span data-stu-id="303e7-209">0</span></span>                                                                                |
| <span data-ttu-id="303e7-210">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-210">Get command:</span></span>     | [<span data-ttu-id="303e7-211">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_test di profondità GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-213">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-213">Description:</span></span>     | <span data-ttu-id="303e7-214">Buffer di profondità abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="303e7-215">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-215">Attribute group:</span></span> | <span data-ttu-id="303e7-216">depth-buffer/Enable</span><span class="sxs-lookup"><span data-stu-id="303e7-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="303e7-217">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-217">Initial value:</span></span>   | <span data-ttu-id="303e7-218">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-219">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-219">Get command:</span></span>     | [<span data-ttu-id="303e7-220">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>funzione di \_ profondità GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-222">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-222">Description:</span></span>     | <span data-ttu-id="303e7-223">Funzione di test del buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="303e7-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="303e7-224">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-224">Attribute group:</span></span> | <span data-ttu-id="303e7-225">buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="303e7-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-226">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-226">Initial value:</span></span>   | <span data-ttu-id="303e7-227">\_meno GL</span><span class="sxs-lookup"><span data-stu-id="303e7-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="303e7-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-228">Get command:</span></span>     | [<span data-ttu-id="303e7-229">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>\_Blend GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-231">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-231">Description:</span></span>     | <span data-ttu-id="303e7-232">Blending abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-232">Blending enabled</span></span>                   |
| <span data-ttu-id="303e7-233">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-233">Attribute group:</span></span> | <span data-ttu-id="303e7-234">colore-buffer/Abilita</span><span class="sxs-lookup"><span data-stu-id="303e7-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="303e7-235">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-235">Initial value:</span></span>   | <span data-ttu-id="303e7-236">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-237">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-237">Get command:</span></span>     | [<span data-ttu-id="303e7-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_src BLENC \_</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-240">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-240">Description:</span></span>     | <span data-ttu-id="303e7-241">Funzione di origine blending</span><span class="sxs-lookup"><span data-stu-id="303e7-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="303e7-242">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-242">Attribute group:</span></span> | <span data-ttu-id="303e7-243">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="303e7-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-244">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-244">Initial value:</span></span>   | <span data-ttu-id="303e7-245">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="303e7-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="303e7-246">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-246">Get command:</span></span>     | [<span data-ttu-id="303e7-247">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>\_DST Blend \_ DST</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-249">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-249">Description:</span></span>     | <span data-ttu-id="303e7-250">Funzione di destinazione di Blend</span><span class="sxs-lookup"><span data-stu-id="303e7-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="303e7-251">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-251">Attribute group:</span></span> | <span data-ttu-id="303e7-252">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="303e7-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-253">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-253">Initial value:</span></span>   | <span data-ttu-id="303e7-254">\_zero GL</span><span class="sxs-lookup"><span data-stu-id="303e7-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="303e7-255">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-255">Get command:</span></span>     | [<span data-ttu-id="303e7-256">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="303e7-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_dithering GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-258">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-258">Description:</span></span>     | <span data-ttu-id="303e7-259">Rethering abilitato</span><span class="sxs-lookup"><span data-stu-id="303e7-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="303e7-260">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-260">Attribute group:</span></span> | <span data-ttu-id="303e7-261">colore-buffer/Abilita</span><span class="sxs-lookup"><span data-stu-id="303e7-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="303e7-262">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-262">Initial value:</span></span>   | <span data-ttu-id="303e7-263">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="303e7-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="303e7-264">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-264">Get command:</span></span>     | [<span data-ttu-id="303e7-265">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_op logica \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="303e7-267">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-267">Description:</span></span>     | <span data-ttu-id="303e7-268">Operazione logica abilitata</span><span class="sxs-lookup"><span data-stu-id="303e7-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="303e7-269">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-269">Attribute group:</span></span> | <span data-ttu-id="303e7-270">colore-buffer/Abilita</span><span class="sxs-lookup"><span data-stu-id="303e7-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="303e7-271">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-271">Initial value:</span></span>   | <span data-ttu-id="303e7-272">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="303e7-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="303e7-273">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-273">Get command:</span></span>     | [<span data-ttu-id="303e7-274">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="303e7-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="303e7-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_ \_ modalità operativa logica \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="303e7-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303e7-276">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="303e7-276">Description:</span></span>     | <span data-ttu-id="303e7-277">Funzione logica Operation</span><span class="sxs-lookup"><span data-stu-id="303e7-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="303e7-278">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="303e7-278">Attribute group:</span></span> | <span data-ttu-id="303e7-279">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="303e7-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="303e7-280">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="303e7-280">Initial value:</span></span>   | <span data-ttu-id="303e7-281">\_copia GL</span><span class="sxs-lookup"><span data-stu-id="303e7-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="303e7-282">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="303e7-282">Get command:</span></span>     | [<span data-ttu-id="303e7-283">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="303e7-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




