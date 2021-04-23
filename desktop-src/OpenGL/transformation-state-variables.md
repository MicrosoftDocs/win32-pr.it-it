---
title: Variabili dello stato della trasformazione
description: Variabili dello stato della trasformazione
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variabili di stato della trasformazione OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908829"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="87e53-104">Variabili dello stato della trasformazione</span><span class="sxs-lookup"><span data-stu-id="87e53-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="87e53-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>MATRICE \_ DI GL MODELVIEW \_</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="87e53-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-106">Property</span></span> | <span data-ttu-id="87e53-107">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="87e53-108">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-108">Description:</span></span>     | <span data-ttu-id="87e53-109">Stack di matrici di Modelview</span><span class="sxs-lookup"><span data-stu-id="87e53-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="87e53-110">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="87e53-111">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-111">Initial value:</span></span>   | <span data-ttu-id="87e53-112">Identità</span><span class="sxs-lookup"><span data-stu-id="87e53-112">Identity</span></span>                           |
| <span data-ttu-id="87e53-113">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-113">Get command:</span></span>     | [<span data-ttu-id="87e53-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="87e53-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="87e53-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>MATRICE DI \_ \_ PROIEZIONE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="87e53-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-116">Property</span></span> | <span data-ttu-id="87e53-117">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-118">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-118">Description:</span></span>     | <span data-ttu-id="87e53-119">Stack matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="87e53-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="87e53-120">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="87e53-121">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-121">Initial value:</span></span>   | <span data-ttu-id="87e53-122">Identità</span><span class="sxs-lookup"><span data-stu-id="87e53-122">Identity</span></span>                                                                       |
| <span data-ttu-id="87e53-123">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-123">Get command:</span></span>     | [<span data-ttu-id="87e53-124">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="87e53-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>MATRICE \_ TRAME GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="87e53-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-126">Property</span></span> | <span data-ttu-id="87e53-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-128">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-128">Description:</span></span>     | <span data-ttu-id="87e53-129">Stack di matrici di trame</span><span class="sxs-lookup"><span data-stu-id="87e53-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="87e53-130">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="87e53-131">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-131">Initial value:</span></span>   | <span data-ttu-id="87e53-132">Identità</span><span class="sxs-lookup"><span data-stu-id="87e53-132">Identity</span></span>                                                                       |
| <span data-ttu-id="87e53-133">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-133">Get command:</span></span>     | [<span data-ttu-id="87e53-134">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="87e53-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ VIEWPORT</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="87e53-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-136">Property</span></span> | <span data-ttu-id="87e53-137">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-138">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-138">Description:</span></span>     | <span data-ttu-id="87e53-139">Origine ed extent del viewport</span><span class="sxs-lookup"><span data-stu-id="87e53-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="87e53-140">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-140">Attribute group:</span></span> | <span data-ttu-id="87e53-141">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="87e53-141">viewport</span></span>                                                                         |
| <span data-ttu-id="87e53-142">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="87e53-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-143">Get command:</span></span>     | [<span data-ttu-id="87e53-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="87e53-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>INTERVALLO DI PROFONDITÀ GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="87e53-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-146">Property</span></span> | <span data-ttu-id="87e53-147">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-148">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-148">Description:</span></span>     | <span data-ttu-id="87e53-149">Intervallo di profondità vicino e lontano</span><span class="sxs-lookup"><span data-stu-id="87e53-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="87e53-150">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-150">Attribute group:</span></span> | <span data-ttu-id="87e53-151">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="87e53-151">viewport</span></span>                                                                       |
| <span data-ttu-id="87e53-152">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-152">Initial value:</span></span>   | <span data-ttu-id="87e53-153">0, 1</span><span class="sxs-lookup"><span data-stu-id="87e53-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="87e53-154">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-154">Get command:</span></span>     | [<span data-ttu-id="87e53-155">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="87e53-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ MODELVIEW \_ STACK \_ DEPTH</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="87e53-157">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-157">Property</span></span> | <span data-ttu-id="87e53-158">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-159">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-159">Description:</span></span>     | <span data-ttu-id="87e53-160">Puntatore dello stack della matrice di Modelview</span><span class="sxs-lookup"><span data-stu-id="87e53-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="87e53-161">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="87e53-162">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-162">Initial value:</span></span>   | <span data-ttu-id="87e53-163">1</span><span class="sxs-lookup"><span data-stu-id="87e53-163">1</span></span>                                                                                |
| <span data-ttu-id="87e53-164">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-164">Get command:</span></span>     | [<span data-ttu-id="87e53-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="87e53-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>PROFONDITÀ \_ \_ DELLO STACK DI PROIEZIONE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="87e53-167">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-167">Property</span></span> | <span data-ttu-id="87e53-168">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-169">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-169">Description:</span></span>     | <span data-ttu-id="87e53-170">Puntatore dello stack della matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="87e53-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="87e53-171">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="87e53-172">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-172">Initial value:</span></span>   | <span data-ttu-id="87e53-173">1</span><span class="sxs-lookup"><span data-stu-id="87e53-173">1</span></span>                                                                                |
| <span data-ttu-id="87e53-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-174">Get command:</span></span>     | [<span data-ttu-id="87e53-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="87e53-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>PROFONDITÀ \_ STACK \_ TRAME GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="87e53-177">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-177">Property</span></span> | <span data-ttu-id="87e53-178">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-179">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-179">Description:</span></span>     | <span data-ttu-id="87e53-180">Puntatore dello stack della matrice di trame</span><span class="sxs-lookup"><span data-stu-id="87e53-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="87e53-181">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="87e53-182">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-182">Initial value:</span></span>   | <span data-ttu-id="87e53-183">1</span><span class="sxs-lookup"><span data-stu-id="87e53-183">1</span></span>                                                                                |
| <span data-ttu-id="87e53-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-184">Get command:</span></span>     | [<span data-ttu-id="87e53-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="87e53-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>MODALITÀ \_ MATRICE GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="87e53-187">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-187">Property</span></span> | <span data-ttu-id="87e53-188">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87e53-189">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-189">Description:</span></span>     | <span data-ttu-id="87e53-190">Modalità matrice corrente</span><span class="sxs-lookup"><span data-stu-id="87e53-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="87e53-191">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-191">Attribute group:</span></span> | <span data-ttu-id="87e53-192">trasformazione</span><span class="sxs-lookup"><span data-stu-id="87e53-192">transform</span></span>                                                                        |
| <span data-ttu-id="87e53-193">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-193">Initial value:</span></span>   | <span data-ttu-id="87e53-194">GL \_ MODELVIEW</span><span class="sxs-lookup"><span data-stu-id="87e53-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="87e53-195">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-195">Get command:</span></span>     | [<span data-ttu-id="87e53-196">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="87e53-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="87e53-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="87e53-198">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-198">Property</span></span> | <span data-ttu-id="87e53-199">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="87e53-200">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-200">Description:</span></span>     | <span data-ttu-id="87e53-201">Normalizzazione normale corrente on/off</span><span class="sxs-lookup"><span data-stu-id="87e53-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="87e53-202">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-202">Attribute group:</span></span> | <span data-ttu-id="87e53-203">transform/enable</span><span class="sxs-lookup"><span data-stu-id="87e53-203">transform/enable</span></span>                    |
| <span data-ttu-id="87e53-204">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-204">Initial value:</span></span>   | <span data-ttu-id="87e53-205">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="87e53-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="87e53-206">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-206">Get command:</span></span>     | [<span data-ttu-id="87e53-207">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="87e53-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="87e53-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="87e53-209">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-209">Property</span></span> | <span data-ttu-id="87e53-210">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="87e53-211">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-211">Description:</span></span>     | <span data-ttu-id="87e53-212">Coefficienti del piano di ritaglio utente</span><span class="sxs-lookup"><span data-stu-id="87e53-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="87e53-213">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-213">Attribute group:</span></span> | <span data-ttu-id="87e53-214">trasformazione</span><span class="sxs-lookup"><span data-stu-id="87e53-214">transform</span></span>                                |
| <span data-ttu-id="87e53-215">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-215">Initial value:</span></span>   | <span data-ttu-id="87e53-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="87e53-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="87e53-217">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-217">Get command:</span></span>     | [<span data-ttu-id="87e53-218">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="87e53-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="87e53-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="87e53-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="87e53-220">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e53-220">Property</span></span> | <span data-ttu-id="87e53-221">Valore</span><span class="sxs-lookup"><span data-stu-id="87e53-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="87e53-222">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="87e53-222">Description:</span></span>     | <span data-ttu-id="87e53-223">*i* th user clipping plane enabled</span><span class="sxs-lookup"><span data-stu-id="87e53-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="87e53-224">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="87e53-224">Attribute group:</span></span> | <span data-ttu-id="87e53-225">transform/enable</span><span class="sxs-lookup"><span data-stu-id="87e53-225">transform/enable</span></span>                   |
| <span data-ttu-id="87e53-226">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="87e53-226">Initial value:</span></span>   | <span data-ttu-id="87e53-227">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="87e53-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="87e53-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="87e53-228">Get command:</span></span>     | [<span data-ttu-id="87e53-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="87e53-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




