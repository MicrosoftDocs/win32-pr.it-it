---
title: Variabili di stato del controllo Framebuffer
description: Variabili di stato del controllo Framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variabili di stato del controllo Framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998414271956de44710e9ef456722d7499adb862
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910079"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="eb060-104">Variabili di stato del controllo Framebuffer</span><span class="sxs-lookup"><span data-stu-id="eb060-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="eb060-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>BUFFER \_ DI DISEGNO GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

| <span data-ttu-id="eb060-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-106">Property</span></span> | <span data-ttu-id="eb060-107">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-107">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="eb060-108">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-108">Description:</span></span>     | <span data-ttu-id="eb060-109">Buffer selezionati per il disegno</span><span class="sxs-lookup"><span data-stu-id="eb060-109">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="eb060-110">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-110">Attribute group:</span></span> | <span data-ttu-id="eb060-111">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="eb060-111">color-buffer</span></span>                           |
| <span data-ttu-id="eb060-112">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-112">Initial value:</span></span>   |                                        |
| <span data-ttu-id="eb060-113">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-113">Get command:</span></span>     | [<span data-ttu-id="eb060-114">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="eb060-114">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="eb060-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_ \_ WRITEMASK DELL'INDICE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="eb060-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-116">Property</span></span> | <span data-ttu-id="eb060-117">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-117">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-118">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-118">Description:</span></span>     | <span data-ttu-id="eb060-119">Maschera di scrittura dell'indice dei colori</span><span class="sxs-lookup"><span data-stu-id="eb060-119">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="eb060-120">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-120">Attribute group:</span></span> | <span data-ttu-id="eb060-121">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="eb060-121">color-buffer</span></span>                                                                     |
| <span data-ttu-id="eb060-122">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-122">Initial value:</span></span>   | <span data-ttu-id="eb060-123">1 di</span><span class="sxs-lookup"><span data-stu-id="eb060-123">1's</span></span>                                                                              |
| <span data-ttu-id="eb060-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-124">Get command:</span></span>     | [<span data-ttu-id="eb060-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="eb060-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK COLORE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="eb060-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-127">Property</span></span> | <span data-ttu-id="eb060-128">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-128">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-129">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-129">Description:</span></span>     | <span data-ttu-id="eb060-130">La scrittura a colori abilita; R, G, B o A</span><span class="sxs-lookup"><span data-stu-id="eb060-130">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="eb060-131">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-131">Attribute group:</span></span> | <span data-ttu-id="eb060-132">color-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-132">color-buffer</span></span>                                                                     |
| <span data-ttu-id="eb060-133">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-133">Initial value:</span></span>   | <span data-ttu-id="eb060-134">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="eb060-134">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="eb060-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-135">Get command:</span></span>     | [<span data-ttu-id="eb060-136">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="eb060-136">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL \_ DEPTH \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="eb060-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-138">Property</span></span> | <span data-ttu-id="eb060-139">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-140">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-140">Description:</span></span>     | <span data-ttu-id="eb060-141">Buffer di profondità abilitato per la scrittura</span><span class="sxs-lookup"><span data-stu-id="eb060-141">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="eb060-142">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-142">Attribute group:</span></span> | <span data-ttu-id="eb060-143">depth-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-143">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="eb060-144">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-144">Initial value:</span></span>   | <span data-ttu-id="eb060-145">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="eb060-145">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="eb060-146">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-146">Get command:</span></span>     | [<span data-ttu-id="eb060-147">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="eb060-147">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL \_ STENCIL \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="eb060-149">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-149">Property</span></span> | <span data-ttu-id="eb060-150">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-151">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-151">Description:</span></span>     | <span data-ttu-id="eb060-152">Maschera di scrittura stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-152">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="eb060-153">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-153">Attribute group:</span></span> | <span data-ttu-id="eb060-154">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="eb060-155">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-155">Initial value:</span></span>   | <span data-ttu-id="eb060-156">1 di</span><span class="sxs-lookup"><span data-stu-id="eb060-156">1's</span></span>                                                                              |
| <span data-ttu-id="eb060-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-157">Get command:</span></span>     | [<span data-ttu-id="eb060-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="eb060-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>VALORE DI \_ CANCELLAZIONE \_ COLORE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="eb060-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-160">Property</span></span> | <span data-ttu-id="eb060-161">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-161">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-162">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-162">Description:</span></span>     | <span data-ttu-id="eb060-163">Valore non crittografato del buffer di colore (modalità RGBA)</span><span class="sxs-lookup"><span data-stu-id="eb060-163">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="eb060-164">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-164">Attribute group:</span></span> | <span data-ttu-id="eb060-165">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="eb060-165">color-buffer</span></span>                                                                   |
| <span data-ttu-id="eb060-166">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-166">Initial value:</span></span>   | <span data-ttu-id="eb060-167">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="eb060-167">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="eb060-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-168">Get command:</span></span>     | [<span data-ttu-id="eb060-169">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="eb060-169">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>VALORE DI \_ CANCELLAZIONE DELL'INDICE GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="eb060-171">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-171">Property</span></span> | <span data-ttu-id="eb060-172">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-172">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-173">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-173">Description:</span></span>     | <span data-ttu-id="eb060-174">Valore di cancellazione del buffer dei colori (modalità color-index)</span><span class="sxs-lookup"><span data-stu-id="eb060-174">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="eb060-175">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-175">Attribute group:</span></span> | <span data-ttu-id="eb060-176">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="eb060-176">color-buffer</span></span>                                                                   |
| <span data-ttu-id="eb060-177">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-177">Initial value:</span></span>   | <span data-ttu-id="eb060-178">0</span><span class="sxs-lookup"><span data-stu-id="eb060-178">0</span></span>                                                                              |
| <span data-ttu-id="eb060-179">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-179">Get command:</span></span>     | [<span data-ttu-id="eb060-180">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="eb060-180">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>VALORE DI \_ CANCELLAZIONE \_ PROFONDITÀ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="eb060-182">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-182">Property</span></span> | <span data-ttu-id="eb060-183">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-184">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-184">Description:</span></span>     | <span data-ttu-id="eb060-185">Valore di cancellazione del buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="eb060-185">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="eb060-186">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-186">Attribute group:</span></span> | <span data-ttu-id="eb060-187">depth-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-187">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="eb060-188">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-188">Initial value:</span></span>   | <span data-ttu-id="eb060-189">1</span><span class="sxs-lookup"><span data-stu-id="eb060-189">1</span></span>                                                                                |
| <span data-ttu-id="eb060-190">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-190">Get command:</span></span>     | [<span data-ttu-id="eb060-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="eb060-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>VALORE DI \_ CANCELLAZIONE STENCIL GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="eb060-193">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-193">Property</span></span> | <span data-ttu-id="eb060-194">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-195">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-195">Description:</span></span>     | <span data-ttu-id="eb060-196">Valore di cancellazione stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-196">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="eb060-197">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-197">Attribute group:</span></span> | <span data-ttu-id="eb060-198">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="eb060-199">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-199">Initial value:</span></span>   | <span data-ttu-id="eb060-200">0</span><span class="sxs-lookup"><span data-stu-id="eb060-200">0</span></span>                                                                                |
| <span data-ttu-id="eb060-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-201">Get command:</span></span>     | [<span data-ttu-id="eb060-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="eb060-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="eb060-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL \_ ACCUM \_ CLEAR \_ VALUE</dt> </span><span class="sxs-lookup"><span data-stu-id="eb060-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="eb060-204">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb060-204">Property</span></span> | <span data-ttu-id="eb060-205">Valore</span><span class="sxs-lookup"><span data-stu-id="eb060-205">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="eb060-206">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="eb060-206">Description:</span></span>     | <span data-ttu-id="eb060-207">Valore di cancellazione del buffer di accumulo</span><span class="sxs-lookup"><span data-stu-id="eb060-207">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="eb060-208">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="eb060-208">Attribute group:</span></span> | <span data-ttu-id="eb060-209">accum-buffer</span><span class="sxs-lookup"><span data-stu-id="eb060-209">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="eb060-210">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="eb060-210">Initial value:</span></span>   | <span data-ttu-id="eb060-211">0</span><span class="sxs-lookup"><span data-stu-id="eb060-211">0</span></span>                                                                              |
| <span data-ttu-id="eb060-212">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="eb060-212">Get command:</span></span>     | [<span data-ttu-id="eb060-213">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="eb060-213">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




